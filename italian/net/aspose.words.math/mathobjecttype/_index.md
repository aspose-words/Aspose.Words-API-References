---
title: Enum MathObjectType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Math.MathObjectType enum. Specifica il tipo di un oggetto Office Math.
type: docs
weight: 4110
url: /it/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Specifica il tipo di un oggetto Office Math.

```csharp
public enum MathObjectType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| OMath | `0` | Istanza di testo matematico. |
| OMathPara | `1` | Paragrafo matematico o zona matematica di visualizzazione che ne contiene uno o piùOMath elementi che sono in modalità di visualizzazione. |
| Accent | `2` | Funzione di accento, composta da una base e un segno diacritico combinato. |
| Bar | `3` | Funzione Bar, composta da un argomento base e un overbar o underbar. |
| BorderBox | `4` | Oggetto Border Box, costituito da un bordo disegnato attorno a un'istanza di testo matematico (come una formula o un'equazione) |
| Box | `5` | Oggetto scatola, utilizzato per raggruppare i componenti di un'equazione o altra istanza di testo matematico. |
| Delimiter | `6` | Oggetto delimitatore, costituito da delimitatori di apertura e chiusura (come parentesi, parentesi graffe , parentesi quadre e barre verticali) e un elemento contenuto all'interno. |
| Degree | `7` | Laurea in matematica radicale. |
| Argument | `8` | Oggetto argomento. Racchiude le entità di Office Math quando vengono utilizzate come argomenti per altre entità di Office Math. |
| Array | `9` | L'oggetto array, costituito da una o più equazioni, espressioni o altro testo matematico, viene eseguito che può essere giustificato verticalmente come un'unità rispetto al testo circostante sulla riga. |
| Fraction | `10` | Oggetto frazione, costituito da un numeratore e un denominatore separati da una barra della frazione. |
| Denominator | `11` | Denominatore di un oggetto frazione. |
| Numerator | `12` | Numeratore dell'oggetto Frazione. |
| Function | `13` | Oggetto Function-Apply, che consiste in un nome di funzione e un elemento argomento su cui si agisce. |
| FunctionName | `14` | Nome della funzione. Ad esempio, i nomi delle funzioni sono sin e cos. |
| GroupCharacter | `15` | Oggetto Group-Character, costituito da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi |
| Limit | `16` | Limite inferiore delLowerLimit oggetto e il limite superiore delUpperLimit funzione. |
| LowerLimit | `17` | Oggetto limite inferiore, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sotto di essa. |
| UpperLimit | `18` | Oggetto limite superiore, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sopra di essa. |
| Matrix | `19` | Oggetto matrice, costituito da uno o più elementi disposti su una o più righe e una o più colonne. |
| MatrixRow | `20` | Singola riga della matrice. |
| NAry | `21` | Oggetto n-ario, costituito da un oggetto n-ario, una base (o operando) e limiti superiore e inferiore opzionali. |
| Phantom | `22` | Oggetto fantasma. |
| Radical | `23` | Oggetto radicale, costituito da un radicale, un elemento base e un grado opzionale . |
| SubscriptPart | `24` | Pedice dell'oggetto che può avere parte pedice. |
| SuperscriptPart | `25` | Apice dell'oggetto apice. |
| PreSubSuperscript | `26` | Oggetto Pre-Sub-Superscript, che consiste in un elemento base e un pedice e un apice posizionati a sinistra della base. |
| Subscript | `27` | Oggetto Subscript, costituito da un elemento base e da uno script di dimensioni ridotte posizionato in basso a destra. |
| SubSuperscript | `28` | Oggetto sotto-apice, che consiste in un elemento base, una scrittura di dimensioni ridotte posizionata sotto a destra e una scrittura di dimensioni ridotte posizionata sopra e a destra. |
| Supercript | `29` | Oggetto apice, costituito da un elemento base e da una scritta di dimensioni ridotte posizionata sopra e a destra. |

### Esempi

Mostra come stampare la struttura dei nodi di ogni nodo matematico di Office in un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Quando facciamo in modo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e poi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di una stringa di tutti i nodi OfficeMath incontrati e dei relativi figli.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ottiene il testo semplice del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Esegui.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi secondari di un nodo OfficeMath sono stati visitati.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga allo StringBuilder e la rientra in base alla profondità con cui si trova il visitatore nell'albero del documento.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Math](../../aspose.words.math/)
* assemblea [Aspose.Words](../../)


