---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FormField Result, hantera och anpassa enkelt strängutdata för dina formulärfält för en förbättrad användarupplevelse.
type: docs
weight: 170
url: /sv/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Hämtar eller anger en sträng som representerar resultatet av detta formulärfält.

```csharp
public string Result { get; set; }
```

## Anmärkningar

För ett textformulärfält är resultatet texten som finns i fältet.

För ett kryssruteformulär kan resultatet vara "1" eller "0" för att indikera markerat eller omarkerat.

För ett rullgardinsmenyfält är resultatet den sträng som valts i rullgardinsmenyn.

Miljö`Result` för ett textformulärfält gäller inte texten format som anges i[`TextInputFormat`](../textinputformat/) Om du vill ange ett värde och använda formatet , använd[`SetTextInputValue`](../settextinputvalue/) metod.

För ett textformulärfält[`TextInputDefault`](../textinputdefault/) värdet tillämpas om*value* är`null`.

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
