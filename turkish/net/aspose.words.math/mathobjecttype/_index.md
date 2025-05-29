---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme için Office Math nesne türlerini kolayca tanımlamak ve yönetmek amacıyla Aspose.Words.Math.MathObjectType enum'unu keşfedin.
type: docs
weight: 4800
url: /tr/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Bir Office Math nesnesinin türünü belirtir.

```csharp
public enum MathObjectType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| OMath | `0` | Matematiksel metin örneği. |
| OMathPara | `1` | Bir veya daha fazla matematik paragrafı veya görüntüleme matematik alanı içerenOMath görüntüleme modunda olan öğeler. |
| Accent | `2` | Bir taban ve birleştirici bir diakritik işaretten oluşan vurgu işlevi. |
| Bar | `3` | Bir temel argüman ve bir üst veya alt çubuktan oluşan Bar fonksiyonu. |
| BorderBox | `4` | Matematiksel metin örneğinin (örneğin bir formül veya denklem) etrafına çizilen bir kenarlıktan oluşan Kenarlık Kutusu nesnesi |
| Box | `5` | Bir denklemin veya matematiksel metnin diğer örneklerinin bileşenlerini gruplamak için kullanılan kutu nesnesi. |
| Delimiter | `6` | Ayırıcı nesnesi, açma ve kapama ayraçlarından (parantez, parantez, köşeli parantez ve dikey çubuklar gibi) ve içinde bulunan bir öğeden oluşur. |
| Degree | `7` | Matematiksel radikalde derece. |
| Argument | `8` | Bağımsız değişken nesnesi. Office Math varlıklarını, diğer Office Math varlıklarına bağımsız değişken olarak kullanıldıklarında çevreler. |
| Array | `9` | Bir veya daha fazla denklem, ifade veya diğer matematiksel metinlerden oluşan dizi nesnesi, satırdaki çevreleyen metne göre bir birim olarak dikey olarak hizalanabilen çalıştırır. |
| Fraction | `10` | Kesir nesnesi, bir kesir çubuğuyla ayrılmış bir pay ve paydadan oluşur. |
| Denominator | `11` | Bir kesir nesnesinin paydası. |
| Numerator | `12` | Kesir nesnesinin Payı. |
| Function | `13` | İşlev-Uygulama nesnesi, bir işlev adı ve üzerinde işlem yapılan bir argüman öğesinden oluşur. |
| FunctionName | `14` | Fonksiyonun adı. Örneğin, fonksiyon adları sin ve cos'tur. |
| GroupCharacter | `15` | Metnin üstüne veya altına çizilen bir karakterden oluşan Grup Karakter nesnesi, genellikle öğeleri görsel olarak gruplandırmak amacıyla kullanılır |
| Limit | `16` | Alt sınırLowerLimit nesne ve üst sınırUpperLimit fonksiyon. |
| LowerLimit | `17` | Alt Sınır nesnesi, taban çizgisindeki metinden ve hemen altındaki küçültülmüş boyuttaki metinden oluşur. |
| UpperLimit | `18` | Taban çizgisindeki metinden ve hemen üstündeki küçültülmüş boyuttaki metinden oluşan Üst Sınır nesnesi. |
| Matrix | `19` | Bir veya daha fazla satırda ve bir veya daha fazla sütunda düzenlenmiş bir veya daha fazla öğeden oluşan matris nesnesi. |
| MatrixRow | `20` | Matrisin tek satırı. |
| NAry | `21` | N-ary nesne, bir n-ary nesneden, bir tabandan (veya işlenenden) ve isteğe bağlı üst ve alt sınırlardan oluşur. |
| Phantom | `22` | Hayalet nesne. |
| Radical | `23` | Radikal nesne, bir radikal, bir temel eleman ve isteğe bağlı bir dereceden oluşur. |
| SubscriptPart | `24` | Alt simge parçası olabilen nesnenin alt simgesi. |
| SuperscriptPart | `25` | Üst simge nesnesinin üst simgesi. |
| PreSubSuperscript | `26` | Bir taban öğesinden ve tabanın soluna yerleştirilmiş bir alt simge ve üst simgeden oluşan Ön-Alt-Üst Simge nesnesi. |
| Subscript | `27` | Bir taban öğesinden ve altına ve sağına yerleştirilmiş küçültülmüş boyutlu bir betikten oluşan alt simge nesnesi. |
| SubSuperscript | `28` | Bir taban öğesinden, altına ve sağa yerleştirilmiş küçültülmüş boyutlu bir betikten ve üstüne ve sağa yerleştirilmiş küçültülmüş boyutlu bir betikten oluşan alt-üst simge nesnesi. |
| Supercript | `29` | Bir taban öğesinden ve üstüne ve sağına yerleştirilmiş küçültülmüş boyutlu bir betikten oluşan üst simge nesnesi. |

## Örnekler

Bir belgedeki her ofis matematik düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ikili olmayan ağacını dolaşır.
/// Karşılaşılan tüm OfficeMath düğümlerinin ve bunların alt öğelerinin bir dize biçiminde bir haritasını oluşturur.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ziyaretçinin topladığı belgenin düz metnini alır.
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
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derine indiğine bağlı olarak girintisini ayarlayın.
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
