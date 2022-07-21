---
title: FieldPrivate
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das PRIVATE-Feld.
type: docs
weight: 2150
url: /de/net/aspose.words.fields/fieldprivate/
---
## FieldPrivate class

Implementiert das PRIVATE-Feld.

```csharp
public class FieldPrivate : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldPrivate](fieldprivate)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Bietet einen privaten Speicherbereich. Dieses Feld wird verwendet, um Daten für Dokumente zu speichern, die aus anderen Dateiformaten konvertiert wurden.

### Beispiele

Zeigt, wie PRIVATE-Felder verarbeitet werden.

```csharp
{
    // Öffnen Sie ein Corel WordPerfect-Dokument, das wir in das .docx-Format konvertiert haben.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x-Dokumente wie das von uns geladene können PRIVATE-Felder enthalten.
    // Microsoft Word behält PRIVATE-Felder während Lade-/Speicheroperationen bei,
    // bietet aber keine Funktionalität für sie.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Wir können auch PRIVATE-Felder mit einem Document Builder einfügen.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Diese Felder sind keine praktikable Methode zum Schutz vertraulicher Informationen.
    // Sofern die Abwärtskompatibilität mit älteren Versionen von WordPerfect nicht unbedingt erforderlich ist,
    // wir können diese Felder sicher entfernen. Wir können dies mit einer DocumentVisiitor-Implementierung tun.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Entfernt alle gefundenen PRIVATE-Felder.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// Wenn der Knoten zu einem PRIVATE-Feld gehört, wird das gesamte Feld entfernt.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
