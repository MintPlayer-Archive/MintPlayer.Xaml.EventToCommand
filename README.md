# MintPlayer.Xaml.EventToCommand
[![NuGet Version](https://img.shields.io/nuget/v/MintPlayer.Xaml.EventToCommand.svg?style=flat)](https://www.nuget.org/packages/MintPlayer.Xaml.EventToCommand)
[![NuGet](https://img.shields.io/nuget/dt/MintPlayer.Xaml.EventToCommand.svg?style=flat)](https://www.nuget.org/packages/MintPlayer.Xaml.EventToCommand)
[![Build Status](https://travis-ci.org/MintPlayer/MintPlayer.Xaml.EventToCommand.svg?branch=master)](https://travis-ci.org/MintPlayer/MintPlayer.Xaml.EventToCommand)
![.NET Core](https://github.com/MintPlayer/MintPlayer.Xaml.EventToCommand/workflows/.NET%20Core/badge.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-green.svg)](https://opensource.org/licenses/Apache-2.0)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/2ae1c816b1c645988c18004ce70fc05c)](https://www.codacy.com/gh/MintPlayer/MintPlayer.Xaml.EventToCommand?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=MintPlayer/MintPlayer.Xaml.EventToCommand&amp;utm_campaign=Badge_Grade)

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

[Official explaination for the Event-To-Command behavior](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/app-fundamentals/behaviors/reusable/event-to-command-behavior)
