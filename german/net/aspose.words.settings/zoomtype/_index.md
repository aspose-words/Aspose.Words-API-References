---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Settings.ZoomType, um die Dokumentanzeigegrößen in Microsoft Word für optimale Anzeige und Produktivität anzupassen.
type: docs
weight: 6810
url: /de/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Mögliche Werte dafür, wie groß oder klein das Dokument in Microsoft Word auf dem Bildschirm angezeigt wird.

```csharp
public enum ZoomType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Custom | `0` | Der Zoomprozentsatz wird explizit festgelegt. Er wird nicht automatisch neu berechnet, wenn sich die Steuerelementgröße ändert. |
| None | `0` | Gibt an, dass der explizite Zoomprozentsatz verwendet werden soll. Dasselbe wieCustom . |
| FullPage | `1` | Der Zoomprozentsatz wird automatisch neu berechnet, um eine ganze Seite auszufüllen. |
| PageWidth | `2` | Der Zoomprozentsatz wird automatisch neu berechnet, um der Seitenbreite zu entsprechen. |
| TextFit | `3` | Der Zoomprozentsatz wird automatisch neu berechnet, damit der Text hineinpasst. |

## Beispiele

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Siehe auch

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
