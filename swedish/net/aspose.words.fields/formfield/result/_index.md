---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words för .NET
description: FormField Result fast egendom. Hämtar eller ställer in en sträng som representerar resultatet av detta formulärfält i C#.
type: docs
weight: 170
url: /sv/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Hämtar eller ställer in en sträng som representerar resultatet av detta formulärfält.

```csharp
public string Result { get; set; }
```

## Anmärkningar

För ett textformulärfält blir resultatet den text som finns i fältet.

För ett kryssrutaformulär kan resultatet vara "1" eller "0" för att indikera markerat eller avmarkerat.

För ett rullgardinsfält är resultatet den sträng som valts i rullgardinsmenyn.

Miljö`Result` för ett textformulärsfält gäller inte textformat som anges i[`TextInputFormat`](../textinputformat/) . Om du vill ställa in ett värde och använda formatet , använd[`SetTextInputValue`](../settextinputvalue/) metod.

För ett textformulärfält[`TextInputDefault`](../textinputdefault/) värde tillämpas if*value* är`null`.

## Exempel

Visar hur man infogar en kombinationsruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Formulärfältet kommer att visas i form av en "select" html-tagg.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Se även

* class [FormField](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
