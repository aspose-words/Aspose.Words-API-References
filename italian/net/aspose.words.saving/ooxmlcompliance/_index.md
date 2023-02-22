---
title: Enum OoxmlCompliance
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.OoxmlCompliance enum. Consente di specificare quale specifica OOXML verrà utilizzata durante il salvataggio nel formato DOCX.
type: docs
weight: 5060
url: /it/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

Consente di specificare quale specifica OOXML verrà utilizzata durante il salvataggio nel formato DOCX.

```csharp
public enum OoxmlCompliance
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Ecma376_2006 | `0` | ECMA-376 1a edizione, 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 Livello di conformità transitorio. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 Rigoroso livello di conformità. |

### Esempi

Mostra come inserire forme DML in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di avvolgimento che possono avere le forme.
// 1 - Fluttuante:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - In linea:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Se devi creare forme "non primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornersRounded, TopCornersRounded, or DiagonalCornersRounded,
// quindi salva il documento con la conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Mostra come configurare un elenco per riavviare la numerazione in ciascuna sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La proprietà "IsRestartAtEachSection" sarà applicabile solo quando
// il livello di conformità OOXML del documento è a uno standard più recente di "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

Mostra come impostare una specifica di conformità OOXML a cui aderire un documento salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se configuriamo le opzioni di compatibilità per essere conformi a Microsoft Word 2003,
// l'inserimento di un'immagine ne definirà la forma usando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
 // qualsiasi documento che salviamo mentre passiamo questo oggetto dovrà seguire quello standard.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Il nostro documento salvato definisce la forma utilizzando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


