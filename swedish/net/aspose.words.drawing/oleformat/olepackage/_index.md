---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till OlePackage-egenskaper för OLE-objekt. Få sömlös integration med OLE-paket och förbättra dina datahanteringsfunktioner.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Ge åtkomst till[`OlePackage`](../../olepackage/) om OLE-objektet är ett OLE-paket. Returnerar`null` annars.

```csharp
public OlePackage OlePackage { get; }
```

## Anmärkningar

OLE-paketet är en äldre teknik som gör det möjligt att omsluta alla filformat som inte finns i OLE-registret för ett Windows-system till ett generiskt paket, vilket gör det möjligt att bädda in nästan vad som helst i ett dokument. Se[`OlePackage`](../../olepackage/) skriv för mer information.

## Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt låter oss öppna andra filer i det lokala filsystemet med hjälp av ett annat installerat program
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
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
