---
title: Lottie
sidebar_label: Lottie
slug: lotie
---

Displays an animation from a Lottie file (URL or local file).

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Examples

[Live example](https://flet-controls-gallery.fly.dev/utility/lottie)

<Tabs groupId="language">
  <TabItem value="python" label="Python" default>

```python
import flet as ft

def main(page: ft.Page):
    page.add(
        ft.Lottie(
            src='https://raw.githubusercontent.com/xvrh/lottie-flutter/master/example/assets/Mobilo/A.json',
            repeat=False,
            reverse=False,
            animate=True
        )
    )

ft.app(target=main)
```

  </TabItem>
</Tabs>

<img src="/img/docs/controls/lottie/basic-lottie.gif" className="screenshot-40" />

## Properties

### `animate`

Whether the animation should be played automatically. Default value is `True`.

### `background_loading`

Whether the animation should be loaded in the background.

### `filter_quality`

The quality of the image layer. Value is of type `FilterQuality` enum and can be one of the
following: `NONE`, `LOW`, `MEDIUM` or `HIGH`. More details on
each [here](https://api.flutter.dev/flutter/dart-ui/FilterQuality.html).

### `fit`

How to inscribe the Lottie composition into the space allocated during layout.

Property value is `ImageFit` enum with supported
values: `NONE`, `CONTAIN`, `COVER`, `FILL`, `FIT_HEIGHT`, `FIT_WIDTH`, `SCALE_DOWN`.

### `repeat`

Whether the animation should repeat in a loop. Default value is `True`.

Has no effect if `animate` is `False`.

### `reverse`

Whether the animation should be played in reverse (from start to end and then continuously from end to start). Default
value is `False`.

Has no effect if `animate` and `repeat` are `False`.

### `src`

The source of the Lottie file. Can be a URL or a local asset file. See [Image.src](/docs/controls/image#src) for more
information about assets.

### `src_base64`

The base64 encoded string of the Lottie file. Either this or `src` must be provided. If both are provided, `src_base64`
will be prioritized/used.

## Events

### `on_error`

Fires when an error occurs while loading the Lottie file.