---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlLoadOptions constructeur. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.
type: docs
weight: 10
url: /de/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public HtmlLoadOptions()
```

### Beispiele

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Wenn der Wert wahr ist, berücksichtigen wir den VML-Code beim Analysieren des geladenen Dokuments.
loadOptions.SupportVml = supportVml;

// Dieses Dokument enthält ein JPEG-Bild in "<!--[if gte vml 1]>" Stichworte,
// und ein anderes PNG-Bild innerhalb von "<![if !vml]>" Stichworte.
// Wenn wir das Flag "SupportVml" auf "true" setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf "false" setzen, lädt Aspose.Words nur das PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../htmlloadoptions/)
* Montage [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments.

```csharp
public HtmlLoadOptions(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann null oder eine leere Zeichenfolge sein. |

### Beispiele

Zeigt, wie ein HTML-Dokument verschlüsselt und dann mit einem Kennwort geöffnet wird.

```csharp
// Erstellen und signieren Sie ein verschlüsseltes HTML-Dokument aus einer verschlüsselten .docx-Datei.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Um dieses Dokument zu laden und zu lesen, müssen wir seine Entschlüsselung bestehen
// Passwort mit einem HtmlLoadOptions-Objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../htmlloadoptions/)
* Montage [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | LoadFormat | Das Format des zu ladenden Dokuments. |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann null oder eine leere Zeichenfolge sein. |
| baseUri | String | Die Zeichenfolge, die verwendet wird, um relative URIs in absolute aufzulösen. Kann null oder eine leere Zeichenfolge sein. |

### Beispiele

Zeigt, wie beim Öffnen eines HTML-Dokuments ein Basis-URI angegeben wird.

```csharp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das durch einen relativen URI verknüpft ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten auflösen.
 // Wir können einen Basis-URI mit einem HtmlLoadOptions-Objekt bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Während das Bild in der Eingabe-.html-Datei beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Siehe auch

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../htmlloadoptions/)
* Montage [Aspose.Words](../../../)


