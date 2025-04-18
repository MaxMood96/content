---
title: "HTMLCanvasElement: width property"
short-title: width
slug: Web/API/HTMLCanvasElement/width
page-type: web-api-instance-property
browser-compat: api.HTMLCanvasElement.width
---

{{APIRef("Canvas API")}}

The **`HTMLCanvasElement.width`** property is a
positive `integer` reflecting the [`width`](/en-US/docs/Web/HTML/Reference/Elements/canvas#width) HTML
attribute of the {{HTMLElement("canvas")}} element interpreted in CSS pixels. When the
attribute is not specified, or if it is set to an invalid value, like a negative, the
default value of `300` is used.

Setting the `width` property resets the entire rendering context to its default state. This includes clearing the canvas (backing buffer), resetting the current path, and resetting _all_ properties like `fillStyle` and `globalCompositeOperation`. This reset occurs for all context types, and occurs even when setting `width` to its current value. To restore the previous content after changing the width, use {{domxref("CanvasRenderingContext2D.getImageData()")}} and {{domxref("CanvasRenderingContext2D.putImageData()")}}. Context properties must be separately tracked and restored.

This is one of the two properties, the other being
{{domxref("HTMLCanvasElement.height")}}, that controls the size of the canvas.

## Value

A number.

## Examples

Given this {{HTMLElement("canvas")}} element:

```html
<canvas id="canvas" width="300" height="300"></canvas>
```

You can get the width of the canvas with the following code:

```js
const canvas = document.getElementById("canvas");
console.log(canvas.width); // 300
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("HTMLCanvasElement")}}: Interface used to define the `HTMLCanvasElement.width` property
- {{domxref("HTMLCanvasElement.height")}}: Other property used to control the size of the canvas
- {{domxref("HTMLEmbedElement.width")}}
- {{domxref("HTMLIFrameElement.width")}}
- {{domxref("HTMLImageElement.width")}}
- {{domxref("HTMLObjectElement.width")}}
- {{domxref("HTMLSourceElement.width")}}
- {{domxref("HTMLVideoElement.width")}}
