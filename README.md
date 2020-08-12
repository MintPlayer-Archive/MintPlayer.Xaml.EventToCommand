# MintPlayer.Xaml.EventToCommand
[![NuGet Version](https://img.shields.io/nuget/v/MintPlayer.Xaml.EventToCommand.svg?style=flat)](https://www.nuget.org/packages/MintPlayer.Xaml.EventToCommand)
[![NuGet](https://img.shields.io/nuget/dt/MintPlayer.Xaml.EventToCommand.svg?style=flat)](https://www.nuget.org/packages/MintPlayer.Xaml.EventToCommand)
[![Build Status](https://travis-ci.org/MintPlayer/MintPlayer.Xaml.EventToCommand.svg?branch=master)](https://travis-ci.org/MintPlayer/MintPlayer.Xaml.EventToCommand)
![.NET Core](https://github.com/MintPlayer/MintPlayer.Xaml.EventToCommand/workflows/.NET%20Core/badge.svg)

This repository contains a behavior that allows you to bind an event to a command in XAML

## Consuming the behavior

    <ListView ItemsSource="{Binding People}">
        <ListView.ItemTemplate>
            <DataTemplate>
                <TextCell Text="{Binding Name}" />
            </DataTemplate>
        </ListView.ItemTemplate>
        <ListView.Behaviors>
            <local:EventToCommandBehavior EventName="ItemSelected" Command="{Binding OutputAgeCommand}" Converter="{StaticResource SelectedItemConverter}" />
        </ListView.Behaviors>
    </ListView>
    <Label Text="{Binding SelectedItemText}" />
    
## Source

https://docs.microsoft.com/en-us/xamarin/xamarin-forms/app-fundamentals/behaviors/reusable/event-to-command-behavior
