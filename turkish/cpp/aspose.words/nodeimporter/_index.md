---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeImporter sınıfı. Bir belgeden diğerine düğümlerin tekrarlı ithalatını verimli bir şekilde gerçekleştirmeyi sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 44000
url: /tr/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Bir belgeden diğerine düğümlerin tekrarlı içe aktarımını verimli bir şekilde gerçekleştirmeye olanak tanır. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class NodeImporter : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Bir belgeden diğerine bir düğüm ithal eder. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | [NodeImporter](./) sınıfının yeni bir örneğini başlatır. |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | [NodeImporter](./) sınıfının yeni bir örneğini başlatır. |
| static [Type](./type/)() |  |
## Açıklamalar


Aspose.Words, Microsoft Word belgeleri arasında parçaları kolayca kopyalama ve taşıma işlevselliği sağlar. Bu, "düğüm ithalatı" olarak bilinir. Bir parçayı bir belgeden diğerine ekleyebilmek için önce onu "ithal" etmeniz gerekir. İthal etme, orijinal düğümün derin bir kopyasını oluşturur ve hedef belgeye eklenmeye hazır hâle getirir.

Bir düğümü ithal etmenin en basit yolu, [ImportNode()](../) yöntemini, [DocumentBase](../documentbase/) nesnesi tarafından sağlanan şekilde kullanmaktır.

Ancak, düğümleri bir belgeden diğerine birden çok kez ithal etmeniz gerektiğinde, [NodeImporter](./) sınıfını kullanmak daha iyidir. [NodeImporter](./) sınıfı, hedef belgede oluşturulan stil ve liste sayısını en aza indirmeyi sağlar.

Bir Microsoft Word belgesinden diğerine parçaları kopyalama veya taşıma, Aspose.Words için bir dizi teknik zorluk ortaya çıkarır. Bir Word belgesinde, stiller ve liste biçimlendirmeleri, belgenin metninden ayrı olarak merkezi bir şekilde depolanır. Paragraflar ve metin akışları yalnızca stillere dahili benzersiz tanımlayıcılarla başvurur.

Zorluklar, stillerin ve listelerin farklı belgelerde farklı olmasından kaynaklanır. Örneğin, bir belgeden diğerine Heading 1 stiliyle biçimlendirilmiş bir paragrafı kopyalamak için dikkate alınması gereken birkaç husus vardır: Heading 1 stilini kaynak belgeden hedef belgeye kopyalayıp kopyalamamaya karar vermek, paragrafı klonlamak, klonlanan paragrafı hedef belgede doğru Heading 1 stiline başvuracak şekilde güncellemek. Stil kopyalanması gerekiyorsa, stilin referans verdiği tüm stiller (stil ve sonraki paragraf stili temelinde) analiz edilmeli ve gerekirse kopyalanmalıdır, vb. Madde işaretli veya numaralı paragrafları kopyalarken benzer sorunlar ortaya çıkar çünkü Microsoft Word, liste tanımlarını metinden ayrı olarak depolar.

[NodeImporter](./) sınıfı, ithalat sırasında "çeviri tablolarını" tutan bir bağlam gibidir. Kaynak ve hedef belgelerdeki stiller ve listeler arasında doğru bir şekilde çeviri yapar.

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
