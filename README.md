# How to add a custom view to a hole in the Xamarin.Forms doughnut chart (SfChart)?

We can add any kind of view to the center of doughnut series using CenterView property. The following code explains how to add image view to the center of doughnut. 

This KB article explains how to add the desired view to a hole in the [doughnut series](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfChart.XForms.DoughnutSeries.html) of [Xamarin.Forms chart](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfChart.XForms.SfChart.html) by using the [CenterView property](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfChart.XForms.DoughnutSeries.html#Syncfusion_SfChart_XForms_DoughnutSeries_CenterView) that has been supported by the [Syncfusion.Xamarin.SfChart](https://www.nuget.org/packages/Syncfusion.Xamarin.SfChart/) version of [16.4.0.41](https://help.syncfusion.com/xamarin/release-notes/v16.2.0.41?type=all#sfchart-features).

Please refer to the following code sample to add the Image view as the center of the doughnut series.

**XAML**
```
<chart:SfChart.Series>
    <chart:DoughnutSeries ItemsSource="{Binding SeriesDataCollection}" 
                          DoughnutCoefficient="0.6" 
                          CircularCoefficient="0.9"
                          XBindingPath="XData" 
                          YBindingPath="YData" >
        <chart:DoughnutSeries.CenterView>
            <StackLayout>
                <Image Source="Avatar2.png" 
                       HeightRequest="80" 
                       WidthRequest="90" 
                       HorizontalOptions="Center" 
                       VerticalOptions="Center"/>
            </StackLayout>
        </chart:DoughnutSeries.CenterView>
</chart:SfChart.Series>
```
**C#**
```
DoughnutSeries doughnutSeries = new DoughnutSeries()
{
    ItemsSource = SeriesDataCollection,
    XBindingPath = "XData",
    YBindingPath = "YData",
};

var centerview = new Image()
{
    Source = "Avatar2.png",
    HeightRequest = 80,
    WidthRequest = 90,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

doughnutSeries.CenterView = centerview;
chart.Series.Add(doughnutSeries);
```

## Output:

![output of centerview of doughtnut series](https://user-images.githubusercontent.com/53489303/200728424-ee8956b2-a603-4f50-b41c-5f24f2146595.png)

KB article - [How to add a custom view to a hole in the Xamarin.Forms doughnut charts](https://www.syncfusion.com/kb/7778/how-to-add-a-custom-view-to-a-hole-in-the-xamarin-forms-doughnut-charts)

## See also

[How to add a custom data marker in Xamarin.Forms Chart](https://www.syncfusion.com/kb/10922/how-to-add-a-custom-data-marker-in-xamarin-forms-chart)

[How to visualize the Xamarin.Forms Pie Chart in linear form](https://www.syncfusion.com/kb/11285/how-to-visualize-the-xamarin-forms-pie-chart-in-linear-form)

[How to apply custom fonts in Xamarin.Forms Chart](https://www.syncfusion.com/kb/9388/how-to-apply-custom-fonts-in-xamarin-forms-chart)

[How to localize the labels in Xamarin.Forms Chart](https://www.syncfusion.com/kb/9415/how-to-localize-the-labels-in-xamarin-forms-chart)
