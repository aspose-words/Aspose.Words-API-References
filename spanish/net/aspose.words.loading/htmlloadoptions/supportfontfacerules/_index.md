---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words para .NET
description: Descubra HtmlLoadOptions SupportFontFaceRules y controle la carga de fuentes fácilmente. Mejore su diseño web habilitando fuentes personalizadas para una apariencia impecable.
type: docs
weight: 60
url: /es/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Obtiene o establece un valor que indica si se deben admitir las reglas @font-face y si se deben cargar las fuentes declaradas. El valor predeterminado es`FALSO` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Observaciones

Si esta opción está habilitada, las fuentes declaradas en las reglas @font-face se cargan y se incrustan en las definiciones de fuentes del documento resultante (consulte[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Esto permite que las fuentes cargadas estén disponibles para renderizar, pero no habilita automáticamente la incrustación de las fuentes al guardar. Para guardar el documento con las fuentes cargadas,[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) propiedad de la[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) La colección debe configurarse en`verdadero` .

Los formatos de fuente admitidos son TTF, EOT y WOFF.

Las reglas @font-face no son compatibles al cargar imágenes SVG.

## Ejemplos

Muestra cómo cargar las reglas declaradas "@font-face".

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
