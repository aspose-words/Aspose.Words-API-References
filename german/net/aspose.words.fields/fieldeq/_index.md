---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldEQ für die nahtlose Implementierung von EQ-Feldern. Verbessern Sie die Dokumentenautomatisierung mit leistungsstarken Funktionen und Flexibilität.
type: docs
weight: 2240
url: /de/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implementiert das EQ-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldEQ : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Das Office Math-Objekt von Returns entsprach dem EQ-Feld. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Beispiele

Zeigt, wie das EQ-Feld durch Office Math ersetzt wird.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Zeigt, wie das EQ-Feld zum Anzeigen verschiedener mathematischer Gleichungen verwendet wird.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ein EQ-Feld zeigt eine mathematische Gleichung an, die aus einem oder mehreren Elementen besteht.
    // Jedes Element hat die folgende Form: [Schalter][Optionen][Argumente].
    // Es kann einen Schalter und mehrere mögliche Optionen geben.
    // Die Argumente sind eine Reihe von durch Kommas getrennten Werten, die in runde Klammern eingeschlossen sind.

    // Hier verwenden wir einen Dokumentgenerator, um ein EQ-Feld mit einem „\f“-Schalter einzufügen, der „Bruch“ entspricht.
    // Wir übergeben die Werte 1 und 4 als Argumente und verwenden keine Optionen.
    // Dieses Feld zeigt einen Bruch mit 1 als Zähler und 4 als Nenner an.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Ein EQ-Feld kann mehrere nacheinander platzierte Elemente enthalten.
    // Wir können Elemente auch ineinander verschachteln, indem wir die inneren Elemente
    // innerhalb der Argumentklammern der äußeren Elemente.
    // Die vollständige Liste der Schalter und ihre Verwendung finden wir hier:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

        // Nachfolgend finden Sie Anwendungen für neun verschiedene EQ-Feldschalter, die wir zum Erstellen verschiedener Arten von Objekten verwenden können.
    // 1 - Array-Schalter "\a", linksbündig, 2 Spalten, 3 Punkte horizontaler und vertikaler Abstand:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Klammerschalter "\b", Klammerzeichen "[", um den Inhalt in eckige Klammern einzuschließen:
    // Beachten Sie, dass wir innerhalb der Klammern ein Array verschachteln, das in der Ausgabe insgesamt wie eine Matrix aussieht.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Verschiebungsschalter "\d", der den Text "B" 30 Stellen nach rechts neben "A" verschiebt und die Lücke als Unterstrich anzeigt:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Formel bestehend aus mehreren Brüchen:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Integralschalter "\i", mit einem Summationssymbol:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Listenschalter "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Wurzelschalter "\r", der eine Kubikwurzel von x anzeigt:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Tiefstellungs-/Hochstellungsschalter "/s", zuerst als Hochstellung und dann als Tiefstellung:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Box-Schalter "\x", mit Linien oben, unten, links und rechts von der Eingabe:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Einige komplexere Kombinationen.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Verwenden Sie einen Dokumentgenerator, um ein EQ-Feld einzufügen, seine Argumente festzulegen und einen neuen Absatz zu beginnen.
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

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
