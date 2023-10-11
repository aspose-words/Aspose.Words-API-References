---
title: OleFormat.OlePackage
second_title: Aspose.Words för .NET API Referens
description: OleFormat fast egendom. Ge åtkomst tillOlePackage om OLEobjekt är ett OLE Package. Returnerarnull annars.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Ge åtkomst till[`OlePackage`](../../olepackage/) om OLE-objekt är ett OLE Package. Returnerar`null` annars.

```csharp
public OlePackage OlePackage { get; }
```

### Anmärkningar

OLE Package är en äldre teknik som gör det möjligt att linda in alla filformat som inte finns i OLE-registret för ett Windows-system till ett generiskt paket som gör det möjligt att bädda in nästan vad som helst i ett dokument. Se[`OlePackage`](../../olepackage/) skriv för mer info.

### Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt tillåter oss att öppna andra filer i det lokala filsystemet med ett annat installerat program
// i vårt operativsystem genom att dubbelklicka på formen som innehåller OLE-objektet i dokumentets brödtext.
// I det här fallet kommer vår externa fil att vara ett ZIP-arkiv.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Se även

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


