---
title: FormField
second_title: Aspose.Words for .NET API Referansı
description: Tek bir form alanını temsil eder.
type: docs
weight: 2460
url: /tr/net/aspose.words.fields/formfield/
---
## FormField class

Tek bir form alanını temsil eder.

```csharp
public class FormField : SpecialChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Belirtilen form alanına yapılan başvurular, alandan her çıkıldığında otomatik olarak güncelleniyorsa doğrudur. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Onay kutusunun boyutunu puan olarak alır veya ayarlar. Sadece ne zaman etkilidir[`IsCheckBoxExactSize`](./ischeckboxexactsize/) doğrudur. |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Onay kutusu form alanının işaretli durumunu alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Onay kutusu form alanının varsayılan değerini alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Açılır form alanının öğelerine erişim sağlar. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Bir açılır form alanında seçili olan öğeyi belirten dizini alır veya ayarlar. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Bir form alanı etkinse doğrudur. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Form alanı için bir giriş makrosu adı döndürür veya ayarlar. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Form alanı için bir çıkış makrosu adı döndürür veya ayarlar. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Odak form alanı olduğunda ve kullanıcı F1'e bastığında bir mesaj kutusunda görüntülenen metni döndürür veya ayarlar. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Metin kutusunun boyutunun otomatik mi yoksa açıkça belirtilmiş mi olduğunu gösteren boole değerini alır veya ayarlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Metin alanı için maksimum uzunluk. Uzunluk sınırlı olmadığında sıfır. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Form alanı adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | İade **DüğümTürü.FormAlanı** . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Odak bir form alanına sahip olduğunda ve kullanıcı F1'e bastığında ileti kutusunda görüntülenen metnin kaynağını belirtir. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Odak bir form alanına sahip olduğunda durum çubuğunda görüntülenen metnin kaynağını belirtir. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Bu form alanının sonucunu temsil eden bir dize alır veya ayarlar. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Odak bir form alanına sahip olduğunda durum çubuğunda görüntülenen metni döndürür veya ayarlar. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Bir metin formu alanının varsayılan dizesini veya hesaplama ifadesini alır veya ayarlar. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Bir metin formu alanı için metin biçimlendirmesini döndürür veya ayarlar. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Bir metin formu alanının türünü alır veya ayarlar. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Form alanı türünü döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Yalnızca form alanı özel karakterini değil, tüm form alanını kaldırır. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | İçinde belirtilen metin biçimini uygular[`TextInputFormat`](./textinputformat/) ve değeri içinde saklar[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Microsoft Word, aşağıdaki form alanlarını sağlar: onay kutusu, metin girişi ve açılır (açılan kutu).

**Form alanı** bir satır içi düğümdür ve yalnızca alt öğesi olabilir **Paragraf**.

**Form alanı** bir belgede özel bir karakterle temsil edilir ve bir metin satırında bir karakter olarak konumlandırılan .

Bir Word belgesindeki eksiksiz bir form alanı, birkaç düğümü tarafından temsil edilen karmaşık bir yapıdır: alan başlangıcı, FORMTEXT gibi alan kodu, form alanı verileri, alan ayırıcı, alan sonucu, alan sonu ve bir yer imi. Bir Word belgesinde programlı olarak form alanları oluşturmak için use [`DocumentBuilder.InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`DocumentBuilder.InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) and [`DocumentBuilder.InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) that tüm form alanı düğümlerinin doğru sırada ve uygun bir durumda oluşturulduğundan emin olun.

### Örnekler

Alan değeri de dahil olmak üzere tüm FormField öğesinin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

Birleşik giriş kutusunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi diziden bir seçenek seçmesine izin verecek bir birleşik giriş kutusu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı bir "select" html etiketi şeklinde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [SpecialChar](../../aspose.words/specialchar/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
