---
title: Class FormField
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FormField sınıf. Tek bir form alanını temsil eder.
type: docs
weight: 2620
url: /tr/net/aspose.words.fields/formfield/
---
## FormField class

Tek bir form alanını temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Form Alanlarıyla Çalışmak](https://docs.aspose.com/words/net/working-with-form-fields/) dokümantasyon makalesi.

```csharp
public class FormField : SpecialChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Belirtilen form alanına yapılan referanslar alandan her çıkıldığında otomatik olarak güncelleniyorsa doğrudur. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Onay kutusunun boyutunu nokta cinsinden alır veya ayarlar. Yalnızca şu durumlarda etkili olur:[`IsCheckBoxExactSize`](./ischeckboxexactsize/) dır-dir`doğru` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Onay kutusu form alanının işaretli durumunu alır veya ayarlar. Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Onay kutusu form alanının varsayılan değerini alır veya ayarlar. Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Açılır form alanının öğelerine erişim sağlar. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Açılır form alanında o anda seçili öğeyi belirten dizini alır veya ayarlar. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Form alanı etkinleştirilmişse doğrudur. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Form alanı için bir giriş makrosu adı döndürür veya ayarlar. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Form alanı için bir çıkış makrosu adı döndürür veya ayarlar. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi formatlamasına erişim sağlar. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Odak form alanı olduğunda ve kullanıcı F1. tuşuna bastığında mesaj kutusunda görüntülenen metni döndürür veya ayarlar. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Metin kutusunun boyutunun otomatik mi yoksa açıkça mı belirtildiğini belirten boole değerini alır veya ayarlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Metin alanı için maksimum uzunluk. Uzunluk sınırlı olmadığında sıfır. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Form alanı adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | İadelerFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Odak bir form alanına geldiğinde ve kullanıcı F1. tuşuna bastığında mesaj kutusunda görüntülenen metnin kaynağını belirtir. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Odak noktası bir form alanı olduğunda durum çubuğunda görüntülenen metnin kaynağını belirtir. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Bu form alanının sonucunu temsil eden bir dize alır veya ayarlar. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Odak noktası bir form alanı olduğunda durum çubuğunda görüntülenen metni döndürür veya ayarlar. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Bir metin formu alanının varsayılan dizesini veya hesaplama ifadesini alır veya ayarlar. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Metin form alanı için metin formatını döndürür veya ayarlar. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Metin form alanının türünü alır veya ayarlar. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Form alanı türünü döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Yalnızca form alanı özel karakterini değil, tüm form alanını kaldırır. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | Belirtilen metin biçimini uygular.[`TextInputFormat`](./textinputformat/) ve değeri içinde saklar[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Microsoft Word aşağıdaki form alanlarını sağlar: onay kutusu, metin girişi ve açılır menü (birleşik kutu).

`FormField`bir satır içi düğümdür ve yalnızca alt öğesi olabilir[`Paragraph`](../../aspose.words/paragraph/).

`FormField` bir belgede özel bir karakterle temsil edilir ve , metin satırındaki bir karakter olarak konumlandırılır.

Bir Word belgesindeki tam form alanı, birkaç düğümle temsil edilen karmaşık bir yapıdır: alan başlangıcı, FORMTEXT gibi alan kodu, form alanı verileri, alan ayırıcı, alan sonucu, alan sonu ve yer işareti. Bir Word belgesinde programlı olarak form alanları oluşturmak için use [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) ve [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) that tüm form alanı düğümlerinin doğru sırada ve uygun durumda oluşturulduğundan emin olun.

### Örnekler

Alan değeri de dahil olmak üzere FormField'ın tamamının nasıl biçimlendirileceğini gösterir.

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

Açılan kutunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dizeden bir seçenek seçmesine olanak tanıyacak bir açılan kutu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı "select" html etiketi şeklinde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [SpecialChar](../../aspose.words/specialchar/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


