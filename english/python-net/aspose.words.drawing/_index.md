---
title: aspose.words.drawing module
linktitle: aspose.words.drawing module
articleTitle: aspose.words.drawing module
second_title: Aspose.Words for Python
description: "The aspose.words.drawing module provides classes that allow to create and modify drawing objects."
type: docs
weight: 70
url: /python-net/aspose.words.drawing/
---

The **aspose.words.drawing** module provides classes that allow to create and modify drawing objects.


All drawing objects in Microsoft Word documents are represented by instances of the [Shape](./shape/) and [GroupShape](./groupshape/) classes.
An object of  the [Shape](./shape/) class is a node in a document and can represent a picture, textbox, AutoShape or an OLE object.


The classes in this module support the latest (Word 2007 - 2013 DrawingML) and the earlier (pre Word 2007 - Office Art) shapes.




## Classes

| Class | Description |
| --- | --- |
| [Adjustment](./adjustment/) | Represents adjustment values that are applied to the specified shape. |
| [AdjustmentCollection](./adjustmentcollection/) | Represents a read-only collection of [Adjustment](./adjustment/) adjust values that are applied to the specified shape. |
| [Fill](./fill/) | Represents fill formatting for an object. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article. |
| [GlowFormat](./glowformat/) | Represents the glow formatting for an object. |
| [GradientStop](./gradientstop/) | Represents one gradient stop. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article. |
| [GradientStopCollection](./gradientstopcollection/) | Contains a collection of [GradientStop](./gradientstop/) objects. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article. |
| [GroupShape](./groupshape/) | Represents a group of shapes in a document. To learn more, visit the [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/python-net/how-to-add-group-shape-into-a-word-document/) documentation article. |
| [HorizontalRuleFormat](./horizontalruleformat/) | Represents horizontal rule formatting. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |
| [ImageData](./imagedata/) | Defines an image for a shape. To learn more, visit the [Working with Images](https://docs.aspose.com/words/python-net/working-with-images/) documentation article. |
| [ImageSize](./imagesize/) | Contains information about image size and resolution. To learn more, visit the [Working with Images](https://docs.aspose.com/words/python-net/working-with-images/) documentation article. |
| [OleFormat](./oleformat/) | Provides access to the data of an OLE object or ActiveX control. To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/python-net/working-with-ole-objects/) documentation article. |
| [OlePackage](./olepackage/) | Allows to access OLE Package properties. To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/python-net/working-with-ole-objects/) documentation article. |
| [ReflectionFormat](./reflectionformat/) | Represents the reflection formatting for an object. |
| [ShadowFormat](./shadowformat/) | Represents shadow formatting for an object. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article. |
| [Shape](./shape/) | Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |
| [ShapeBase](./shapebase/) | Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |
| [SignatureLine](./signatureline/) | Provides access to signature line properties. To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article. |
| [SoftEdgeFormat](./softedgeformat/) | Represents the soft edge formatting for an object. |
| [Stroke](./stroke/) | Defines a stroke for a shape. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |
| [TextBox](./textbox/) | Defines attributes that specify how a text is displayed inside a shape. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |
| [TextPath](./textpath/) | Defines the text and formatting of the text path (of a WordArt object). To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article. |

## Enumerations

| Enumeration | Description |
| --- | --- |
| [ArrowLength](./arrowlength/) | Length of the arrow at the end of a line. |
| [ArrowType](./arrowtype/) | Specifies the type of an arrow at a line end. |
| [ArrowWidth](./arrowwidth/) | Width of the arrow at the end of a line. |
| [DashStyle](./dashstyle/) | Dashed line style. |
| [EndCap](./endcap/) | Specifies line cap style. |
| [FillType](./filltype/) | Specifies fill type for a fillable object. |
| [FlipOrientation](./fliporientation/) | Possible values for the orientation of a shape. |
| [GradientStyle](./gradientstyle/) | Specifies the style for a gradient fill. |
| [GradientVariant](./gradientvariant/) | Specifies the variant for a gradient fill. |
| [HorizontalAlignment](./horizontalalignment/) | Specifies horizontal alignment of a floating shape, text frame or floating table. |
| [HorizontalRuleAlignment](./horizontalrulealignment/) | Represents the alignment for the specified horizontal rule. |
| [ImageType](./imagetype/) | Specifies the type (format) of an image in a Microsoft Word document. |
| [JoinStyle](./joinstyle/) | Line join style. |
| [LayoutFlow](./layoutflow/) | Determines the flow of the text layout in a textbox. |
| [PatternType](./patterntype/) | Specifies the fill pattern to be used to fill a shape. |
| [PresetTexture](./presettexture/) | Specifies texture to be used to fill a shape. |
| [RelativeHorizontalPosition](./relativehorizontalposition/) | Specifies to what the horizontal position of a shape or text frame is relative. |
| [RelativeHorizontalSize](./relativehorizontalsize/) | Specifies relatively to what the width of a shape or a text frame is calculated horizontally. |
| [RelativeVerticalPosition](./relativeverticalposition/) | Specifies to what the vertical position of a shape or text frame is relative. |
| [RelativeVerticalSize](./relativeverticalsize/) | Specifies relatively to what the height of a shape or a text frame is calculated vertically. |
| [ShadowType](./shadowtype/) | Specifies the type of a shape shadow. |
| [ShapeLineStyle](./shapelinestyle/) | Specifies the compound line style of a [Shape](./shape/). |
| [ShapeMarkupLanguage](./shapemarkuplanguage/) | Specifies Markup language used for the shape. |
| [ShapeTextOrientation](./shapetextorientation/) | Specifies orientation of text in shapes. |
| [ShapeType](./shapetype/) | Specifies the type of shape in a Microsoft Word document. |
| [TextBoxAnchor](./textboxanchor/) | Specifies values used for shape text vertical alignment. |
| [TextBoxWrapMode](./textboxwrapmode/) | Specifies how text wraps inside a shape. |
| [TextPathAlignment](./textpathalignment/) | WordArt alignment. |
| [TextureAlignment](./texturealignment/) | Specifies the alignment for the tiling of the texture fill. |
| [VerticalAlignment](./verticalalignment/) | Specifies vertical alignment of a floating shape, text frame or a floating table. |
| [WrapSide](./wrapside/) | Specifies what side(s) of the shape or picture the text wraps around. |
| [WrapType](./wraptype/) | Specifies how text is wrapped around a shape or picture. |

