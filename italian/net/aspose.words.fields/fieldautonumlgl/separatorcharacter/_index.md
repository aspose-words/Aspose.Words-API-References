---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words per .NET
description: Scopri come personalizzare la proprietà FieldAutoNumLgl SeparatorCharacter per migliorare la formattazione dei dati con un carattere separatore flessibile.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Ottiene o imposta il carattere separatore da utilizzare.

```csharp
public string SeparatorCharacter { get; set; }
```

## Esempi

Mostra come organizzare un documento utilizzando i campi AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // I campi AUTONUMLGL visualizzano un numero che aumenta in ogni campo AUTONUMLGL all'interno del suo attuale livello di intestazione.
    // Questi campi mantengono un conteggio separato per ogni livello di intestazione,
     // e ogni campo visualizza anche i conteggi dei campi AUTONUMLGL per tutti i livelli di intestazione al di sotto del proprio.
    // La modifica del conteggio per un qualsiasi livello di intestazione reimposta i conteggi per tutti i livelli superiori a 1.
    // Questo ci consente di organizzare il nostro documento sotto forma di elenco schematico.
    // Questo è il primo campo AUTONUMLGL a livello di intestazione 1, che visualizza "1." nel documento.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Questo è il secondo campo AUTONUMLGL a livello di intestazione 1, quindi visualizzerà "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Questo è il primo campo AUTONUMLGL a livello di intestazione 2,
    // e il conteggio AUTONUMLGL per il livello di intestazione sottostante è "2", quindi verrà visualizzato "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Questo è il primo campo AUTONUMLGL a livello di intestazione 3.
    // Funziona allo stesso modo del campo sopra, verrà visualizzato "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Questo campo si trova a un livello di intestazione pari a 2 e il suo rispettivo conteggio AUTONUMLGL è pari a 2, quindi il campo visualizzerà "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incremento del conteggio AUTONUMLGL per un livello di intestazione inferiore a questo
    // ha reimpostato il conteggio per questo livello in modo che questo campo visualizzi "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Il carattere separatore, che appare nel risultato del campo subito dopo il numero,
        // è un punto fermo per impostazione predefinita. Se lasciamo questa proprietà nulla,
        // il nostro ultimo campo AUTONUMLGL visualizzerà "2.2.1." nel documento.
        Assert.IsNull(field.SeparatorCharacter);

        // Impostazione di un carattere separatore personalizzato e rimozione del punto finale
        // cambierà l'aspetto del campo da "2.2.1." a "2:2:1".
        // Applicheremo questo a tutti i campi che abbiamo creato.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire una clausola numerata da un campo AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Questo testo apparterrà al campo legale auto num sopra di esso.
    // Si chiuderà quando faremo clic sulla freccia accanto al campo AUTONUMLGL corrispondente in Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Guarda anche

* class [FieldAutoNumLgl](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
