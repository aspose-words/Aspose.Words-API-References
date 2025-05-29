---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Math.MathObjectType per identificare e gestire facilmente i tipi di oggetti di Office Math per un'elaborazione avanzata dei documenti.
type: docs
weight: 4800
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
| OMathPara | `1` | Paragrafo matematico o zona di visualizzazione matematica che contiene uno o piùOMath elementi che sono in modalità di visualizzazione. |
| Accent | `2` | Funzione di accento, costituita da una base e da un segno diacritico di combinazione. |
| Bar | `3` | Funzione barra, composta da un argomento base e da una barra superiore o inferiore. |
| BorderBox | `4` | Oggetto Border Box, costituito da un bordo disegnato attorno a un'istanza di testo matematico (ad esempio una formula o un'equazione) |
| Box | `5` | Oggetto box, utilizzato per raggruppare i componenti di un'equazione o di un'altra istanza di testo matematico. |
| Delimiter | `6` | Oggetto delimitatore, costituito da delimitatori di apertura e chiusura (come parentesi, graffe, quadre e barre verticali) e un elemento contenuto al suo interno. |
| Degree | `7` | Laurea in matematica radicale. |
| Argument | `8` | Oggetto argomento. Racchiude le entità di Office Math quando vengono utilizzate come argomenti per altre entità di Office Math. |
| Array | `9` | Oggetto array, costituito da una o più equazioni, espressioni o altri testi matematici che possono essere giustificati verticalmente come un'unità rispetto al testo circostante sulla riga. |
| Fraction | `10` | Oggetto frazione, costituito da un numeratore e un denominatore separati da una barra di frazione. |
| Denominator | `11` | Denominatore di un oggetto frazione. |
| Numerator | `12` | Numeratore dell'oggetto Frazione. |
| Function | `13` | Oggetto Funzione-Applica, che consiste in un nome di funzione e un elemento argomento su cui si agisce. |
| FunctionName | `14` | Nome della funzione. Ad esempio, i nomi delle funzioni sono sin e cos. |
| GroupCharacter | `15` | Oggetto di gruppo-carattere, costituito da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi |
| Limit | `16` | Limite inferiore delLowerLimit oggetto e il limite superiore delUpperLimit funzione. |
| LowerLimit | `17` | Oggetto di limite inferiore, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sotto di esso. |
| UpperLimit | `18` | Oggetto Upper-Limit, costituito da testo sulla linea di base e testo di dimensioni ridotte immediatamente sopra di esso. |
| Matrix | `19` | Oggetto matrice, costituito da uno o più elementi disposti su una o più righe e una o più colonne. |
| MatrixRow | `20` | Singola riga della matrice. |
| NAry | `21` | Oggetto n-ario, costituito da un oggetto n-ario, una base (o operando) e limiti superiori e inferiori facoltativi. |
| Phantom | `22` | Oggetto fantasma. |
| Radical | `23` | Oggetto radicale, costituito da un radicale, un elemento base e un grado facoltativo . |
| SubscriptPart | `24` | Indice dell'oggetto che può avere una parte indice. |
| SuperscriptPart | `25` | Apice dell'oggetto apice. |
| PreSubSuperscript | `26` | Oggetto Pre-Sub-Superscript, costituito da un elemento base e da un pedice e un apice posizionati a sinistra della base. |
| Subscript | `27` | Oggetto indice, costituito da un elemento base e da uno script di dimensioni ridotte posizionato sotto e a destra. |
| SubSuperscript | `28` | Oggetto sub-apice, costituito da un elemento base, uno script di dimensioni ridotte posizionato in basso e a destra e uno script di dimensioni ridotte posizionato in alto e a destra. |
| Supercript | `29` | Oggetto apice, costituito da un elemento base e da uno script di dimensioni ridotte posizionato sopra e a destra. |

## Esempi

Mostra come stampare la struttura di ogni nodo matematico d'ufficio in un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Quando otteniamo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e quindi attraversa tutti i nodi figlio in modalità depth-first.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi OfficeMath rilevati e dei relativi elementi figlio.
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
    /// Chiamato quando nel documento viene rilevato un nodo Run.
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
    /// Chiamato dopo che sono stati visitati tutti i nodi figlio di un nodo OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiungere una riga allo StringBuilder e rientrarla a seconda della profondità a cui si trova il visitatore nell'albero del documento.
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
