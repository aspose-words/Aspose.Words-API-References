---
title: MathObjectType
second_title: Aspose.Words per .NET API Reference
description: Specifica il tipo di un oggetto Office Math.
type: docs
weight: 3870
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
| OMathPara | `1` | Paragrafo matematico, o visualizza la zona matematica, che ne contiene uno o piùOMath elementi che sono in modalità di visualizzazione. |
| Accent | `2` | Funzione di accento, costituita da una base e un segno diacritico combinato. |
| Bar | `3` | Funzione della barra, costituita da un argomento di base e una barra di sopra o di barra. |
| BorderBox | `4` | Oggetto Border Box, costituito da un bordo disegnato attorno a un'istanza di testo matematico (come una formula o un'equazione) |
| Box | `5` | Oggetto Box, utilizzato per raggruppare i componenti di un'equazione o un'altra istanza di testo matematico. |
| Delimiter | `6` | Oggetto delimitatore, costituito da delimitatori di apertura e chiusura (come parentesi, parentesi graffe, parentesi e barre verticali) e un elemento contenuto all'interno. |
| Degree | `7` | Laurea nel radicale matematico. |
| Argument | `8` | Oggetto argomento. Racchiude le entità di Office Math quando vengono utilizzate come argomenti per altre entità di Office Math. |
| Array | `9` | L'oggetto Array, costituito da una o più equazioni, espressioni o altro testo matematico, esegue che può essere giustificato verticalmente come unità rispetto al testo circostante sulla riga. |
| Fraction | `10` | Oggetto Frazione, costituito da numeratore e denominatore separati da una barra di frazione. |
| Denominator | `11` | Denominatore di un oggetto frazione. |
| Numerator | `12` | Numeratore dell'oggetto Frazione. |
| Function | `13` | Oggetto Function-Apply, che consiste in un nome di funzione e un elemento argomento su cui si agisce. |
| FunctionName | `14` | Nome della funzione. Ad esempio, i nomi delle funzioni sono sin e cos. |
| GroupCharacter | `15` | Oggetto Gruppo-Carattere, costituito da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi |
| Limit | `16` | Limite inferiore delLowerLimit oggetto e il limite superiore delUpperLimit funzione. |
| LowerLimit | `17` | Oggetto limite inferiore, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sotto di essa. |
| UpperLimit | `18` | Oggetto limite superiore, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sopra di esso. |
| Matrix | `19` | Oggetto Matrix, costituito da uno o più elementi disposti in una o più righe e una o più colonne. |
| MatrixRow | `20` | Riga singola della matrice. |
| NAry | `21` | Oggetto N-ario, costituito da un oggetto n-ario, una base (o operando) e limiti superiore e inferiore opzionali. |
| Phantom | `22` | Oggetto fantasma. |
| Radical | `23` | Oggetto radicale, costituito da un radicale, un elemento base e un grado opzionale . |
| SubscriptPart | `24` | Pedice dell'oggetto che può avere pedice parte. |
| SuperscriptPart | `25` | Apice dell'oggetto apice. |
| PreSubSuperscript | `26` | Oggetto Pre-Sub-apice, che consiste in un elemento base e un pedice e apice posti a sinistra della base. |
| Subscript | `27` | Oggetto Pedice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato in basso ea destra. |
| SubSuperscript | `28` | Oggetto Sub-apice, che consiste in un elemento base, uno script di dimensioni ridotte posizionato sotto ea destra e uno script di dimensioni ridotte posizionato sopra ea destra. |
| Supercript | `29` | Oggetto Apice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sopra ea destra. |

### Esempi

Mostra come stampare la struttura del nodo di ogni nodo matematico dell'ufficio in un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Quando otteniamo un nodo composito per accettare un visitatore del documento, il visitatore visita il nodo di accettazione,
    // e quindi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario di nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi OfficeMath incontrati e dei relativi figli.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo OfficeMath nel documento.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo OfficeMath sono stati visitati.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga a StringBuilder e la indenta in base alla profondità del visitatore nell'albero del documento.
    /// </summary>
    /// <nome parametro="testo"></param>
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
