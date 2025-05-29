---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode SetRestrictedTypes in ReportingEngine die Sicherheit erhöht, indem sie den Mitgliederzugriff in der Vorlagensyntax für eine optimierte Datenberichterstattung beschränkt.
type: docs
weight: 80
url: /de/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Gibt Typen an, deren Mitglieder sowie Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| types | Type[] | Einzuschränkende Typen. |

## Bemerkungen

Eingeschränkte Typen sollten vor dem ersten Erstellen eines Berichts festgelegt werden. Nach`BuildReport` aufgerufen wird, können eingeschränkte Typen nicht geändert werden, und beim Versuch, dies zu tun, wird eine Ausnahme ausgelöst. Der beste Ort zum Festlegen eingeschränkter Typen ist der Anwendungsstart.

Beachten Sie, dass eine große Anzahl eingeschränkter Typen die Leistung beeinträchtigen kann. Daher ist es besser, nur diejenigen Typen einzuschränken, deren Zugriff auf die Mitglieder wirklich sensibel ist.

WürfeArgumentException in den folgenden Fällen:

-*types* ist null.

- Einer von*types* Artikel ist`null`.

- Einer von*types* items stellt einen unsichtbaren Typ dar, also einen nicht öffentlichen Typ oder einen öffentlichen verschachtelten Typ, der einen nicht öffentlichen äußeren Typ hat.

- Einer von*types* Elemente stellen einen Array-Typ dar.

-*types* doppelte Einträge enthalten.

## Beispiele

Zeigt, wie der Zugriff auf Mitglieder von Typen verweigert wird, die als unsicher gelten.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Beachten Sie, dass Sie während oder nach dem Erstellen eines Berichts keine eingeschränkten Typen festlegen können.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Wir setzen die Option „AllowMissingMembers“, um Ausnahmen beim Erstellen eines Berichts zu vermeiden.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Wir erhalten eine leere Zeichenfolge, da wir nicht auf die Methode GetType() zugreifen können.
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Siehe auch

* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
