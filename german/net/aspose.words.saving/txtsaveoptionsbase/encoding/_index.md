---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Textexporte mit der Encoding-Eigenschaft von TxtSaveOptionsBase optimieren. Legen Sie einfach Kodierungsoptionen für eine nahtlose UTF-8-Textformatierung fest.
type: docs
weight: 10
url: /de/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Gibt die Kodierung an, die beim Exportieren in Textformate verwendet werden soll. Der Standardwert ist**Kodierung.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

## Beispiele

Zeigt, wie die Kodierung für ein TXT-Ausgabedokument festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie Text mit Zeichen außerhalb des ASCII-Zeichensatzes hinzu.
builder.Write("À È Ì Ò Ù.");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Überprüfen Sie, ob die Eigenschaft „Encoding“ die entsprechende Kodierung für den Inhalt unseres Dokuments enthält.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// Die Verwendung einer ungeeigneten Kodierung kann zum Verlust von Dokumentinhalten führen.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Siehe auch

* class [TxtSaveOptionsBase](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
