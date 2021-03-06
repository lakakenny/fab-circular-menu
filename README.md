# FAB Circular Menu 
[![Pub](https://img.shields.io/pub/v/fab_circular_menu.svg)](https://pub.dev/packages/fab_circular_menu)
[![Pull Requests are welcome](https://img.shields.io/badge/license-MIT-blue)](https://github.com/marianocordoba/fab-circular-menu/blob/master/LICENSE)
[![Pull Requests are welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](https://github.com/marianocordoba/fab-circular-menu/pulls)
[![Codemagic build status](https://api.codemagic.io/apps/5cf6ad31434563000a9534d5/5cf6ad31434563000a9534d4/status_badge.svg)](https://codemagic.io/apps/5cf6ad31434563000a9534d5/5cf6ad31434563000a9534d4/latest_build)

A Flutter package to create a nice circular menu using a Floating Action Button.

Inspired by [Mayur Kshirsagar](https://dribbble.com/mayurksgr)'s great [FAB Microinteraction](https://dribbble.com/shots/4354100-Daily-UI-Challenge-Day-75-FAB-Microinteraction) design.

![Showcase](https://i.imgur.com/vjAvdoR.gif)

## Getting started

Wrap your content with `FabCircularMenu` and set your desired `options`:


```dart
MaterialApp(
  home: Scaffold(
    body: FabCircularMenu(
      child: Placeholder(), // Replace this with your content
      options: <Widget>[
        IconButton(icon: Icon(Icons.home), onPressed: () {
          print('Pressed!');
        })
      ]
    )
  )
)
```

### Options

| Property | Type | Description | Default | Caveat |
|----------|------|-------------|---------|------------|
| <font color="ff0000">`required`</font> child | Widget | The child of this widget | - 
| <font color="ff0000">`required`</font> options | List<Widget> | The available options of the menu | -
| ringColor | Color | The color of the ring | `Colors.white`
| ringDiameter | double | The diameter of the ring | `screenWidth * 1.2`
| ringWidth | double | The width of the ring | `ringDiameter / 3`
| fabMargin | EdgeInsets | The margin around the FAB | `EdgeInsets.all(24.0)`
| fabColor | Color | The color of the FAB | `primaryColor` |
| fabOpenColor | Color | The color of the FAB when opened | `primaryColor` | Will override `fabColor` for open state
| fabCloseColor | Color | The color of the FAB when closed | `primaryColor` | Will override `fabColor` for close state
| fabOpenIcon | Icon | The open icon | `Icon(Icons.menu)`
| fabCloseIcon | Icon | The close icon | `Icon(Icons.close)`
| animationDuration | Duration | The animation duration | `Duration(milliseconds: 800)`
| onDisplayChange | Function | A callback called when the open/close state changes | `Function`
| controller | FabCircularMenuController | A controller for opening or closing the menu | `null`