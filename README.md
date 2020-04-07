# How-to-add-custom-view-in-the-center-view-of-Xamarin.Forms-DoughnutSeries-chart-SfChart-

We can add any kind of view to the center of doughnut series using CenterView property. The following code explains how to add image view to the center of doughnut. 

XAML:
. . .
<chart:SfChart.Series>
    <chart:DoughnutSeries ItemsSource="{Binding SeriesDataCollection}" 
                          DoughnutCoefficient="0.6" 
                          CircularCoefficient="0.9"
                          XBindingPath="XData" 
                          YBindingPath="YData" >
        <chart:DoughnutSeries.CenterView>
            <StackLayout>
                <Image Source="Avatar14.png" 
                       HeightRequest="80" 
                       WidthRequest="90" 
                       HorizontalOptions="Center" 
                       VerticalOptions="Center"/>
            </StackLayout>
        </chart:DoughnutSeries.CenterView>
</chart:SfChart.Series>
. . .

C#:
DoughnutSeries doughnutSeries = new DoughnutSeries()
{
    ItemsSource = SeriesDataCollection,
    XBindingPath = "XData",
    YBindingPath = "YData",
};

var centerview = new Image()
{
    Source = "Avatar14.png",
    HeightRequest = 80,
    WidthRequest = 90,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

doughnutSeries.CenterView = centerview;
chart.Series.Add(doughnutSeries);

