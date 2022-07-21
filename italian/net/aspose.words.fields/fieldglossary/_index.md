---
title: FieldGlossary
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo GLOSSARIO.
type: docs
weight: 1810
url: /it/net/aspose.words.fields/fieldglossary/
---
## FieldGlossary class

Implementa il campo GLOSSARIO.

```csharp
public class FieldGlossary : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldGlossary](fieldglossary)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryName](../../aspose.words.fields/fieldglossary/entryname) { get; set; } | Ottiene o imposta il nome della voce del glossario da inserire. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Inserisce una voce di glossario.

### Esempi

Mostra come visualizzare un building block con i campi AUTOTEXT e GLOSSARY.

```csharp
Document doc = new Document();

// Crea un documento di glossario e aggiungi un blocco predefinito di glossario.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Crea una fonte e aggiungila come testo al nostro blocco di costruzione.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Imposta un file che contenga parti che il nostro documento o il modello allegato potrebbero non contenere.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per utilizzare i campi per visualizzare il contenuto del nostro blocco predefinito.
// 1 - Utilizzo di un campo AUTOTEXT:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Utilizzo di un campo GLOSSARIO:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
