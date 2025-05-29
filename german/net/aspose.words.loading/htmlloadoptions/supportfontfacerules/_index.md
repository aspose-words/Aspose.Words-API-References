---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words für .NET
description: Entdecken Sie HtmlLoadOptions SupportFontFaceRules und steuern Sie das Laden von Schriftarten ganz einfach. Verbessern Sie Ihr Webdesign mit benutzerdefinierten Schriftarten für einen eleganten Look.
type: docs
weight: 60
url: /de/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob @font-face-Regeln unterstützt werden und ob deklarierte Schriftarten geladen werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Bemerkungen

Wenn diese Option aktiviert ist, werden die in @font-face-Regeln deklarierten Schriftarten geladen und in die Schriftartdefinitionen des resultierenden Dokuments eingebettet (siehe[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Dadurch werden die geladenen Schriftarten für die Darstellung verfügbar, aber aktiviert nicht automatisch die Einbettung der Schriftarten beim Speichern. Um das Dokument mit geladenen Schriftarten zu speichern, die[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) Eigentum der[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) Sammlung sollte eingestellt werden auf`WAHR` .

Unterstützte Schriftformate sind TTF, EOT und WOFF.

@font-face-Regeln werden beim Laden von SVG-Bildern nicht unterstützt.

## Beispiele

Zeigt, wie deklarierte „@font-face“-Regeln geladen werden.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
