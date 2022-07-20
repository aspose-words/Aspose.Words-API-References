---
title: MathObjectType
second_title: Aspose.Words for .NET API Referansı
description: Office Math nesnesinin türünü belirtir.
type: docs
weight: 3870
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
| OMathPara | `1` | Bir veya daha fazlasını içeren matematik paragrafı veya ekran matematik bölgesiOMath görüntüleme modunda olan öğeler. |
| Accent | `2` | Bir taban ve birleştirici aksan işaretinden oluşan vurgu işlevi. |
| Bar | `3` | Temel argüman ve bir üst veya alt çizgiden oluşan çubuk işlevi. |
| BorderBox | `4` | Bir matematiksel metin örneğinin (formül veya denklem gibi) etrafına çizilen bir kenarlıktan oluşan Border Box nesnesi |
| Box | `5` | Bir denklemin bileşenlerini veya başka bir matematiksel metin örneğini gruplamak için kullanılan kutu nesnesi. |
| Delimiter | `6` | Açma ve kapama sınırlayıcılarından (parantezler, parantezler, parantezler ve dikey çubuklar gibi) ve içeride bulunan bir öğeden oluşan sınırlayıcı nesne. |
| Degree | `7` | Matematiksel kökteki derece. |
| Argument | `8` | Bağımsız değişken nesnesi. Diğer Office Math varlıklarına bağımsız değişken olarak kullanıldıklarında Office Math varlıklarını kapsar. |
| Array | `9` | Bir veya daha fazla denklem, ifade veya diğer matematiksel metinlerden oluşan dizi nesnesi, satırda çevreleyen metne göre bir birim olarak dikey olarak hizalanabilen çalıştırmalarından oluşur. |
| Fraction | `10` | Kesir çubuğuyla ayrılmış pay ve paydadan oluşan kesir nesnesi. |
| Denominator | `11` | Bir kesir nesnesinin paydası. |
| Numerator | `12` | Fraction nesnesinin payı. |
| Function | `13` | Bir işlev adından ve üzerinde işlem yapılan bir bağımsız değişken öğesinden oluşan İşlev-Uygula nesnesi. |
| FunctionName | `14` | İşlevin adı. Örneğin, işlev adları sin ve cos. şeklindedir. |
| GroupCharacter | `15` | Metnin üstüne veya altına çizilen bir karakterden oluşan Grup-Karakter nesnesi, genellikle öğeleri görsel olarak gruplandırmak amacıyla |
| Limit | `16` | Alt limitLowerLimit nesne ve üst sınırıUpperLimit işlev. |
| LowerLimit | `17` | Satır taban çizgisindeki metinden ve hemen altındaki küçültülmüş metinden oluşan Alt Sınırlı nesne. |
| UpperLimit | `18` | Satır taban çizgisindeki metinden ve hemen üstündeki küçültülmüş metinden oluşan Üst Sınır nesnesi. |
| Matrix | `19` | Bir veya daha fazla satırda ve bir veya daha fazla sütunda düzenlenmiş bir veya daha fazla öğeden oluşan matris nesnesi. |
| MatrixRow | `20` | Matrisin tek satırı. |
| NAry | `21` | N-ary nesne, bir taban (veya işlenen) ve isteğe bağlı üst ve alt sınırlardan oluşan N-ary nesne. |
| Phantom | `22` | Hayali nesne. |
| Radical | `23` | Bir kökten, bir temel öğeden ve isteğe bağlı bir dereceden oluşan radikal nesne . |
| SubscriptPart | `24` | Alt simge parçasına sahip olabilen nesnenin alt simgesi. |
| SuperscriptPart | `25` | Üst simge nesnesinin üst simgesi. |
| PreSubSuperscript | `26` | Bir temel öğeden ve tabanın soluna yerleştirilmiş bir alt simge ve üst simgeden oluşan Ön Alt Üst Simge nesnesi. |
| Subscript | `27` | Bir temel öğeden ve aşağıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir komut dosyasından oluşan alt simge nesnesi. |
| SubSuperscript | `28` | Bir temel öğe, aşağıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir komut dosyası ve yukarıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir komut dosyasından oluşan alt üst simge nesnesi. |
| Supercript | `29` | Bir temel öğeden ve yukarıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir komut dosyasından oluşan üst simge nesnesi. |

### Örnekler

Bir belgedeki her ofis matematik düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından tüm düğümün alt öğelerini derinlik öncelikli bir şekilde çaprazlar.
    // Ziyaretçi, ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğümler ağacında çapraz geçiş yapar.
/// Karşılaşılan tüm OfficeMath düğümlerinin ve bunların alt öğelerinin bir dizesi biçiminde bir harita oluşturur.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ziyaretçi tarafından toplanan belgenin düz metnini alır.
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
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak girinti yapın.
    /// </summary>
    /// <param name="metin"></param>
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

* ad alanı [Aspose.Words.Math](../../aspose.words.math)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
