---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldEQ per un'implementazione fluida dei campi EQ. Migliora l'automazione dei documenti con potenti funzionalità e flessibilità.
type: docs
weight: 2240
url: /it/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implementa il campo EQ.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldEQ : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Costruttore |

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
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Restituisce l'oggetto Office Math corrispondente al campo EQ. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Esempi

Mostra come sostituire il campo EQ con Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Mostra come utilizzare il campo EQ per visualizzare diverse equazioni matematiche.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Un campo EQ visualizza un'equazione matematica composta da uno o più elementi.
    // Ogni elemento assume la seguente forma: [switch][opzioni][argomenti].
    // Potrebbe esserci un solo interruttore e diverse opzioni possibili.
    // Gli argomenti sono un insieme di valori separati da virgole e racchiusi tra parentesi graffe.

    // Qui utilizziamo un generatore di documenti per inserire un campo EQ, con un'opzione "\f", che corrisponde a "Frazione".
    // Passeremo i valori 1 e 4 come argomenti e non utilizzeremo alcuna opzione.
    // Questo campo visualizzerà una frazione con 1 come numeratore e 4 come denominatore.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Un campo EQ può contenere più elementi posizionati in sequenza.
    // Possiamo anche annidare gli elementi l'uno dentro l'altro posizionando gli elementi interni
    // all'interno delle parentesi quadrate degli argomenti degli elementi esterni.
    // Possiamo trovare l'elenco completo degli switch, insieme ai loro utilizzi, qui:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // Di seguito sono riportate le applicazioni di nove diversi interruttori di campo EQ che possiamo utilizzare per creare diversi tipi di oggetti.
    // 1 - Array switch "\a", allineato a sinistra, 2 colonne, 3 punti di spaziatura orizzontale e verticale:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Commutatore di parentesi quadre "\b", carattere di parentesi quadre "[", per racchiudere il contenuto tra parentesi quadre:
    // Nota che stiamo annidando un array all'interno delle parentesi, che nel complesso apparirà come una matrice nell'output.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Interruttore di spostamento "\d", che sposta il testo "B" di 30 spazi a destra di "A", visualizzando lo spazio vuoto come una sottolineatura:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Formula composta da più frazioni:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Commutatore integrale "\i", con simbolo di sommatoria:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Elenca l'interruttore "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Commutatore radicale "\r", che visualizza la radice cubica di x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Commutazione apice/pedice "/s", prima come apice e poi come pedice:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Casella di controllo "\x", con linee in alto, in basso, a sinistra e a destra dell'input:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Alcune combinazioni più complesse.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Utilizzare un generatore di documenti per inserire un campo EQ, impostarne gli argomenti e iniziare un nuovo paragrafo.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
