---
permalink: /en-US/animations/rotation.htm
title: Rotation XAML and Code Animation for UWP Community Toolkit
description: The Rotation animation behavior allows users to modify and animate the control's rotation 
keywords: windows, app, toolkit, Rotation animation, Rotation, XAML, UWP, animate rotation, behavior
layout: default
search.product: eADQiWindows 10XVcnh
---

# Rotation
The **Rotation animation behavior** allows users to modify and animate the control's rotation. Parameters include: angle values, time, pause delay, duration, and diameter.

## Syntax
```xaml
   <behaviors:Rotation x:Name="RotationBehavior" 
				Value="180"
				CenterX="0.0" 
				CenterY="0.0" 
				CenterZ="0.0" 
				Duration="1.5" 
				Delay="0.5" 
				AutomaticallyStart="True"/>
  </behaviors:Rotation>
```

or directly from code:

```C#
MyRectangle.Rotate(
                duration: Duration,
                delay: Delay,
                value: (float)Value,
                centerX: (float)CenterX,
                centerY: (float)CenterY,
                centerZ: (float)CenterZ);
    
```

Behavior animations can also be chained and awaited.

```C#
    Element.Rotate(duration: 0.3, value: 30f).StartAsync();

    await Element.Rotate(duration: 0.3, value: 30f).StartAsync();

    var anim = element.Rotate(value: 30f).Opacity(value: 0.5).Blur(blurAmount:5);
    anim.SetDurationForAll(2);
    anim.Completed += animation_completed;
    anim.StartAsync();

    anim.Stop();
```

[Rotation Behavior Sample Page Source](https://github.com/Microsoft/UWPCommunityToolkit/tree/master/Microsoft.Toolkit.Uwp.SampleApp/SamplePages/RotationBehavior)
## Example Image

## Platforms

Windows 10 SDK 10585 or higher

## API

Please view the [toolkit sample application](https://github.com/Microsoft/UWPCommunityToolkit/tree/master/Microsoft.Toolkit.Uwp.SampleApp) for the UWP Community Toolkit for current samples and example code.