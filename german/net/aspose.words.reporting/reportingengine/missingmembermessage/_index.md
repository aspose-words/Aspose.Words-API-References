---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words für .NET
description: Entdecken Sie die MissingMemberMessage-Eigenschaft der ReportingEngine und passen Sie Nachrichten für fehlende Objektmitglieder ganz einfach an. Verbessern Sie mühelos das Benutzererlebnis!
type: docs
weight: 30
url: /de/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Ruft einen Zeichenfolgenwert ab oder legt ihn fest, der anstelle eines Vorlagenausdrucks ausgegeben wird und einen einfachen Verweis auf ein fehlendes Element eines Objekts darstellt. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string MissingMemberMessage { get; set; }
```

## Bemerkungen

Die Eigenschaft sollte in Verbindung mit demAllowMissingMembers -Option. Andernfalls wird eine Ausnahme ausgelöst, wenn ein fehlendes Mitglied eines Objekts gefunden wird.

Die Eigenschaft betrifft nur die Ausgabe eines Vorlagenausdrucks, der einen einfachen Verweis auf ein fehlendes Objektelement darstellt. Beispielsweise ist die Ausgabe eines binären Operators, dessen Operand auf ein fehlendes Objektelement verweist, nicht betroffen.

Der Wert dieser Eigenschaft kann nicht auf null gesetzt werden.

## Beispiele

Zeigt, wie fehlende Mitglieder zugelassen werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Siehe auch

* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
