
Xamarin.Forms.DataGrid
===================

DataGrid library for Xamarin.Forms Application.



> **Supported Platforms**
  >- Android
  >- iOS
  >- UWP
  >- Windows Store
  >- Windows Phone

#### <i class="icon-pencil"></i> Usage
```
    xmlns:dg="clr-namespace:Xamarin.Forms.DataGrid;assembly=Xamarin.Forms.DataGrid"
    xmlns:conv="clr-namespace:DataGridSample.Views.Converters;assembly=DataGridSample"

<dg:DataGrid ItemsSource="{Binding Teams}" RowHeight="45" HeaderHeight="50" 
             BorderColor="#CCCCCC" HeaderBackground="#E0E6F8">
  <dg:DataGrid.HeaderFontSize>
    <OnIdiom  x:TypeArguments="x:Double">
      <OnIdiom.Tablet>15</OnIdiom.Tablet>
      <OnIdiom.Phone>13</OnIdiom.Phone>
    </OnIdiom>
  </dg:DataGrid.HeaderFontSize>
  <dg:DataGrid.Columns>
    <dg:DataGridColumn Title="Team" PropertyName="Name" Width="3*"/>
    <dg:DataGridColumn Title="Win" PropertyName="Win" />
    <dg:DataGridColumn Title="Loose" PropertyName="Loose" />
    <dg:DataGridColumn Title="Home" PropertyName="Home"/>
    <dg:DataGridColumn Title="Road" PropertyName="Road"/>
    <dg:DataGridColumn Title="Percentage" PropertyName="Percentage" StringFormat="{}{0:0.00}" />
    <dg:DataGridColumn Title="Streak" PropertyName="Streak" Width="0.7*">
      <dg:DataGridColumn.CellTemplate>
        <DataTemplate>
          <ContentView HorizontalOptions="Fill" VerticalOptions="Fill"
                       BackgroundColor="{Binding Streak,Converter={StaticResource StreakToColorConverter}}">
            <Label Text="{Binding Streak}" HorizontalOptions="Center" VerticalOptions="Center" TextColor="Black"/>
          </ContentView>
        </DataTemplate>
      </dg:DataGridColumn.CellTemplate>
    </dg:DataGridColumn>
  </dg:DataGrid.Columns>
  <dg:DataGrid.RowsBackgroundColorPalette>
    <dg:PaletteCollection>
      <Color>#F2F2F2</Color>
      <Color>#FFFFFF</Color>
    </dg:PaletteCollection>
  </dg:DataGrid.RowsBackgroundColorPalette>
  <dg:DataGrid.Resources>
    <ResourceDictionary>
      <conv:StreakToColorConverter x:Key="StreakToColorConverter"/>
    </ResourceDictionary>
  </dg:DataGrid.Resources>
</dg:DataGrid>
```
Screenshots ([see all](https://github.com/akgulebubekir/Xamarin.Forms.DataGrid/tree/master/Screenshots))
-------------

![Screenshots](https://raw.githubusercontent.com/akgulebubekir/Xamarin.Forms.DataGrid/dev/Screenshots/AllinOne.png)