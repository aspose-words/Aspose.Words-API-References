---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Math.MathObjectType, um Office Math-Objekttypen für eine verbesserte Dokumentverarbeitung einfach zu identifizieren und zu verwalten.
type: docs
weight: 4800
url: /de/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Gibt den Typ eines Office Math-Objekts an.

```csharp
public enum MathObjectType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| OMath | `0` | Instanz eines mathematischen Textes. |
| OMathPara | `1` | Mathe-Absatz oder Anzeigemathematikzone, die einen oder mehrereOMath Elemente, die sich im Anzeigemodus befinden. |
| Accent | `2` | Akzentfunktion, bestehend aus einer Basis und einem verbindenden diakritischen Zeichen. |
| Bar | `3` | Balkenfunktion, bestehend aus einem Basisargument und einem Über- oder Unterstrich. |
| BorderBox | `4` | Border-Box-Objekt, bestehend aus einem Rahmen, der um eine Instanz mathematischen Textes (wie etwa eine Formel oder Gleichung) gezeichnet wird |
| Box | `5` | Box-Objekt, das zum Gruppieren von Komponenten einer Gleichung oder einer anderen Instanz mathematischen Textes verwendet wird. |
| Delimiter | `6` | Trennzeichenobjekt, bestehend aus öffnenden und schließenden Trennzeichen (wie Klammern, geschweiften Klammern, eckigen Klammern und senkrechten Strichen) und einem darin enthaltenen Element. |
| Degree | `7` | Abschluss im mathematischen Radikal. |
| Argument | `8` | Argumentobjekt. Umschließt Office Math-Entitäten, wenn sie als Argumente für andere Office Math-Entitäten verwendet werden. |
| Array | `9` | Array-Objekt, bestehend aus einer oder mehreren Gleichungen, Ausdrücken oder anderen mathematischen Textzeilen , die vertikal als Einheit in Bezug auf den umgebenden Text in der Zeile ausgerichtet werden können. |
| Fraction | `10` | Bruchobjekt, bestehend aus Zähler und Nenner, getrennt durch einen Bruchstrich. |
| Denominator | `11` | Nenner eines Bruchobjekts. |
| Numerator | `12` | Zähler des Bruchobjekts. |
| Function | `13` | Function-Apply-Objekt, das aus einem Funktionsnamen und einem Argumentelement besteht, auf das eingewirkt wird. |
| FunctionName | `14` | Name der Funktion. Funktionsnamen sind beispielsweise sin und cos. |
| GroupCharacter | `15` | Gruppenzeichenobjekt, bestehend aus einem Zeichen, das über oder unter Text gezeichnet wird, oft mit dem Zweck, Elemente visuell zu gruppieren |
| Limit | `16` | Untergrenze derLowerLimit Objekt und die Obergrenze desUpperLimit Funktion. |
| LowerLimit | `17` | Unteres Limit-Objekt, bestehend aus Text auf der Grundlinie und verkleinertem Text direkt darunter. |
| UpperLimit | `18` | Obergrenzenobjekt, bestehend aus Text auf der Grundlinie und verkleinertem Text direkt darüber. |
| Matrix | `19` | Matrixobjekt, bestehend aus einem oder mehreren Elementen, die in einer oder mehreren Zeilen und einer oder mehreren Spalten angeordnet sind. |
| MatrixRow | `20` | Einzelne Zeile der Matrix. |
| NAry | `21` | N-äres Objekt, bestehend aus einem n-ären Objekt, einer Basis (oder einem Operanden) und optionalen Ober- und Untergrenzen. |
| Phantom | `22` | Phantomobjekt. |
| Radical | `23` | Radikalobjekt, bestehend aus einem Radikal, einem Basiselement und einem optionalen Grad . |
| SubscriptPart | `24` | Index des Objekts, das einen tiefgestellten Teil haben kann. |
| SuperscriptPart | `25` | Hochgestelltes Objekt des hochgestellten Objekts. |
| PreSubSuperscript | `26` | Pre-Sub-Superscript-Objekt, das aus einem Basiselement und einem links von der Basis platzierten tiefgestellten und hochgestellten Zeichen besteht. |
| Subscript | `27` | Subscript-Objekt, das aus einem Basiselement und einem verkleinerten Script besteht, das rechts darunter platziert ist. |
| SubSuperscript | `28` | Hochgestelltes Objekt, das aus einem Basiselement, einer verkleinerten Schrift darunter rechts und einer verkleinerten Schrift darüber rechts besteht. |
| Supercript | `29` | Hochgestelltes Objekt, das aus einem Basiselement und einer verkleinerten Schrift rechts darüber besteht. |

## Beispiele

Zeigt, wie die Knotenstruktur jedes Office-Mathematikknotens in einem Dokument gedruckt wird.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten in einer Tiefensuche.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte in Form einer Zeichenfolge aller gefundenen OfficeMath-Knoten und ihrer untergeordneten Knoten.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein OfficeMath-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines OfficeMath-Knotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügen Sie dem StringBuilder eine Zeile hinzu und rücken Sie sie ein, je nachdem, wie tief der Besucher im Dokumentbaum ist.
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

### Siehe auch

* namensraum [Aspose.Words.Math](../../aspose.words.math/)
* Montage [Aspose.Words](../../)
