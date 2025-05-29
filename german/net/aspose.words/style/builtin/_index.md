---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words für .NET
description: Finden Sie heraus, ob eine Formatvorlage in MS Word integriert ist. Optimieren Sie Ihr Dokumentdesign mit unserem umfassenden Leitfaden zu den integrierten Formatvorlagen von Word!
type: docs
weight: 40
url: /de/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist.

```csharp
public bool BuiltIn { get; }
```

## Beispiele

Zeigt, wie benutzerdefinierte Stile von integrierten Stilen unterschieden werden.

```csharp
Document doc = new Document();

// Wenn wir ein Dokument mit Microsoft Word oder programmgesteuert mit Aspose.Words erstellen,
// Das Dokument wird mit einer Sammlung von Stilen geliefert, die auf den Text angewendet werden können, um dessen Erscheinungsbild zu ändern.
// Wir können auf diese integrierten Stile über die „Styles“-Sammlung des Dokuments zugreifen.
// Bei allen diesen Stilen ist das Flag „BuiltIn“ auf „true“ gesetzt.
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Erstellen Sie einen benutzerdefinierten Stil und fügen Sie ihn der Sammlung hinzu.
    // Bei benutzerdefinierten Stilen wie diesem wird das Flag „BuiltIn“ auf „false“ gesetzt.
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
