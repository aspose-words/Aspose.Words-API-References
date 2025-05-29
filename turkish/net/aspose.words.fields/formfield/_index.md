---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: .NET için Aspose.Words
description: Belgelerinizde gelişmiş kullanıcı etkileşimi için özelleştirilebilir form alanlarını kolayca oluşturmak ve yönetmek amacıyla Aspose.Words.Fields.FormField sınıfını keşfedin.
type: docs
weight: 3030
url: /tr/net/aspose.words.fields/formfield/
---
## FormField class

Tek bir form alanını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Form Alanlarıyla Çalışma](https://docs.aspose.com/words/net/working-with-form-fields/) belgeleme makalesi.

```csharp
public class FormField : SpecialChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Belirtilen form alanına yapılan başvurular, alandan çıkıldığında otomatik olarak güncelleniyorsa doğrudur. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Onay kutusunun boyutunu noktalar halinde alır veya ayarlar. Yalnızca şu durumlarda etkilidir:[`IsCheckBoxExactSize`](./ischeckboxexactsize/) dır`doğru` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Onay kutusu form alanının işaretli durumunu alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Onay kutusu form alanının varsayılan değerini alır veya ayarlar. Bu özellik için varsayılan değer şudur:`YANLIŞ` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Bir açılır form alanının öğelerine erişim sağlar. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Açılır form alanında şu anda seçili öğeyi belirten dizini alır veya ayarlar. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Bir form alanı etkinleştirilmişse doğrudur. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Form alanı için bir giriş makrosu adı döndürür veya ayarlar. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Form alanı için bir çıkış makrosu adı döndürür veya ayarlar. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Form alanı odakta olduğunda ve kullanıcı F1'e bastığında bir ileti kutusunda görüntülenen metni döndürür veya ayarlar. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Metin kutusunun boyutunun otomatik mi yoksa açıkça mı belirtildiğini belirten Boole değerini alır veya ayarlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinleştirilmişken Microsoft Word'de nesnenin biçimlendirmesinin değiştirilmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Metin alanı için maksimum uzunluk. Uzunluk sınırlı olmadığında sıfır. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Form alan adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | Geri DöndürürFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Bir form alanı odakta olduğunda ve kullanıcı F1'e bastığında bir ileti kutusunda görüntülenen metnin kaynağını belirtir. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Bir form alanı odakta olduğunda durum çubuğunda görüntülenen metnin kaynağını belirtir. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Bu form alanının sonucunu temsil eden bir dize alır veya ayarlar. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Bir form alanı odakta olduğunda durum çubuğunda görüntülenen metni döndürür veya ayarlar. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Bir metin form alanının varsayılan dizesini veya hesaplama ifadesini alır veya ayarlar. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Bir metin form alanı için metin biçimlendirmesini döndürür veya ayarlar. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Bir metin form alanının türünü alır veya ayarlar. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Form alan türünü döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Sadece form alanı özel karakterini değil, tüm form alanını kaldırır. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | Belirtilen metin biçimini uygular[`TextInputFormat`](./textinputformat/) ve değeri depolar[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Microsoft Word aşağıdaki form alanlarını sağlar: onay kutusu, metin girişi ve açılır liste (combobox).

`FormField` bir satır içi düğümdür ve yalnızca bir çocuğu olabilir[`Paragraph`](../../aspose.words/paragraph/).

`FormField` Bir belgede özel bir karakterle temsil edilir ve bir metin satırı içerisinde bir karakter olarak konumlandırılır.

Word belgesindeki tam bir form alanı, birkaç düğümle temsil edilen karmaşık bir yapıdır: alan başlangıcı, FORMTEXT gibi alan kodu, form alanı verileri, alan ayırıcı, alan sonucu, alan sonu ve bir yer imi. Word belgesinde programatik olarak form alanları oluşturmak için kullanın[`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) ve [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/)which tüm form alanı düğümlerinin doğru sırada ve uygun bir durumda oluşturulduğundan emin olun.

## Örnekler

Alan değeri dahil olmak üzere tüm FormField'ın nasıl biçimlendirileceğini gösterir.

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

Bir açılır kutunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dize arasından bir seçenek seçmesine izin verecek bir açılır kutu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı "select" html etiketi biçiminde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [SpecialChar](../../aspose.words/specialchar/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
