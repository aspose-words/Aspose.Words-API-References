---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldEmbed per un'implementazione ottimale dei campi EMBED, migliorando la funzionalità e la versatilità dei documenti.
type: docs
weight: 2260
url: /it/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Implementa il campo EMBED.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldEmbed : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Esempi

Mostra come vengono gestiti alcuni vecchi campi di Microsoft Word, ad esempio SHAPE e EMBED, durante il caricamento.

```csharp
// Aprire un documento creato in Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Se apriamo il documento Word e premiamo Alt+F9, vedremo un campo SHAPE e un campo EMBED.
// Un campo SHAPE è l'ancora/tela per un oggetto AutoShape con lo stile di avvolgimento "In linea con il testo" abilitato.
// Un campo EMBED ha la stessa funzione, ma per un oggetto incorporato,
// ad esempio un foglio di calcolo da un documento Excel esterno.
// Tuttavia, questi campi non appariranno nella raccolta Campi del documento.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Questi campi sono supportati solo dalle vecchie versioni di Microsoft Word.
// Il processo di caricamento del documento convertirà questi campi in oggetti Shape,
// a cui possiamo accedere nella raccolta di nodi del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Il primo nodo Shape corrisponde al campo SHAPE nel documento di input,
// che è l'area di disegno in linea per AutoShape.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Il secondo nodo Forma è l'AutoForma stessa.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// La terza forma è il campo EMBED che conteneva il foglio di calcolo esterno.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
