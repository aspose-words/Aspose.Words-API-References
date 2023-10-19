---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words for .NET
description: Aspose.Words.Math.MathObjectType Sıralama. Office Math nesnesinin türünü belirtir C#'da.
type: docs
weight: 4110
url: /tr/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Office Math nesnesinin türünü belirtir.

```csharp
public enum MathObjectType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| OMath | `0` | Matematiksel metin örneği. |
| OMathPara | `1` | Bir veya daha fazlasını içeren matematik paragrafı veya matematik bölgesini görüntülemeOMath görüntüleme modundaki öğeler. |
| Accent | `2` | Bir taban ve birleştirici aksan işaretinden oluşan vurgu işlevi. |
| Bar | `3` | Temel bağımsız değişken ve üst veya alt çubuktan oluşan çubuk işlevi. |
| BorderBox | `4` | Matematiksel bir metin örneğinin (formül veya denklem gibi) etrafına çizilen bir kenarlıktan oluşan Kenarlık Kutusu nesnesi |
| Box | `5` | Bir denklemin bileşenlerini veya başka bir matematiksel metin örneğini gruplamak için kullanılan Box nesnesi. |
| Delimiter | `6` | Açma ve kapama sınırlayıcılarından (parantez, ayraçları, ayraçlar ve dikey çubuklar gibi) ve içinde yer alan bir öğeden oluşan sınırlayıcı nesnesi. |
| Degree | `7` | Matematiksel radikalin derecesi. |
| Argument | `8` | Bağımsız değişken nesnesi. Diğer Office Math varlıklarına bağımsız değişken olarak kullanıldıklarında Office Math varlıklarını kapsar. |
| Array | `9` | Bir veya daha fazla denklemden, ifadeden veya satırdaki çevredeki metne göre bir birim olarak dikey olarak yaslanabilen diğer matematiksel metin çalıştırmalarından oluşan dizi nesnesi. |
| Fraction | `10` | Kesir çubuğuyla ayrılmış bir pay ve paydadan oluşan kesir nesnesi. |
| Denominator | `11` | Kesir nesnesinin paydası. |
| Numerator | `12` | Kesir nesnesinin payı. |
| Function | `13` | Bir işlev adından ve üzerinde işlem yapılan bir bağımsız değişken öğesinden oluşan Function-Apply nesnesi. |
| FunctionName | `14` | Fonksiyonun adı. Örneğin işlev adları sin ve cos. 'dir. |
| GroupCharacter | `15` | Grup-Karakter nesnesi, metnin üstüne veya altına çizilen bir karakterden oluşur; öğeleri görsel olarak gruplandırmak amacıyla genellikle 'dir |
| Limit | `16` | Alt limitLowerLimit nesne ve üst sınırıUpperLimit function. |
| LowerLimit | `17` | Taban çizgisindeki metinden ve hemen altındaki küçültülmüş boyutlu metinden oluşan Alt Limit nesnesi. |
| UpperLimit | `18` | Taban çizgisindeki metinden ve hemen üstündeki küçültülmüş boyutlu metinden oluşan Üst Sınır nesnesi. |
| Matrix | `19` | Bir veya daha fazla satır ve bir veya daha fazla sütun halinde düzenlenmiş bir veya daha fazla öğeden oluşan Matrix nesnesi. |
| MatrixRow | `20` | Matrisin tek satırı. |
| NAry | `21` | N-ary nesnesi, N-ary nesnesi, bir taban (veya işlenen) ve isteğe bağlı üst ve alt limitlerden oluşur. |
| Phantom | `22` | Hayalet nesne. |
| Radical | `23` | Radikal nesne, bir radikal, bir temel öğe ve isteğe bağlı bir dereceden oluşan . |
| SubscriptPart | `24` | Alt simge kısmına sahip olabilecek nesnenin alt simgesi. |
| SuperscriptPart | `25` | Üst simge nesnesinin üst simgesi. |
| PreSubSuperscript | `26` | Bir temel öğe ve tabanın soluna yerleştirilen bir alt simge ve üst simgeden oluşan Ön Alt Üst Simge nesnesi. |
| Subscript | `27` | Bir temel öğeden ve aşağıya ve sağa yerleştirilen küçültülmüş boyutlu bir komut dosyasından oluşan alt simge nesnesi. |
| SubSuperscript | `28` | Bir temel öğeden, aşağıya ve sağa yerleştirilen küçültülmüş boyutlu bir komut dosyasından ve yukarıya ve sağa yerleştirilen küçültülmüş boyutlu bir komut dosyasından oluşan alt üst simge nesnesi. |
| Supercript | `29` | Bir temel öğeden ve yukarıya ve sağa yerleştirilen küçültülmüş boyutlu bir komut dosyasından oluşan üst simge nesnesi. |

## Örnekler

Bir belgedeki her ofis matematik düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Bir belge ziyaretçisini kabul edecek bileşik bir düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından düğümün tüm alt öğelerini derinlik öncelikli bir şekilde geçer.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğüm ağacını geçer.
/// Karşılaşılan tüm OfficeMath düğümleri ve bunların alt öğelerinden oluşan bir dize biçiminde bir harita oluşturur.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir OfficeMath düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir OfficeMath düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak onu girintileyin.
    /// </summary>
    /// <param adı="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Math](../../aspose.words.math/)
* toplantı [Aspose.Words](../../)
