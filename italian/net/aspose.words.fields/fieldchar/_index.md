---
title: FieldChar Class
linktitle: FieldChar
articleTitle: FieldChar
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldChar, la base essenziale per i caratteri dei campi del documento, che migliora l'elaborazione e la personalizzazione dei documenti.
type: docs
weight: 2080
url: /it/net/aspose.words.fields/fieldchar/
---
## FieldChar class

Classe base per i nodi che rappresentano i caratteri di campo in un documento.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public abstract class FieldChar : SpecialChar
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Restituisce il tipo del campo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Ottiene o imposta se il campo padre è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | RestituisceSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Restituisce un campo per il campo char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ottiene il carattere speciale rappresentato da questo nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Un campo completo in un documento di Microsoft Word è una struttura complessa composta da un carattere di inizio campo, un codice campo, un carattere separatore campo, un risultato campo e un carattere di fine campo. Alcuni campi hanno solo inizio campo, codice campo e fine campo.

Per inserire facilmente un nuovo campo in un documento, utilizzare[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Metodo .

## Esempi

Mostra come lavorare con un nodo FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Recupera l'oggetto facciata che rappresenta il campo nel documento.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Aggiorna il campo per mostrare la data corrente.
field.Update();
```

### Guarda anche

* class [FieldStart](../fieldstart/)
* class [FieldSeparator](../fieldseparator/)
* class [FieldEnd](../fieldend/)
* class [SpecialChar](../../aspose.words/specialchar/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
