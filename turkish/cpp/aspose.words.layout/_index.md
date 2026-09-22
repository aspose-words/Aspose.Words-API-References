---
title: "Aspose::Words::Layout ad alanı"
linktitle: "Aspose::Words::Layout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout ad alanı. Aspose.Words.Layout ad alanı, C++'ta belge sayfalara biçimlendirildiğinde, belirli belge öğelerinin hangi sayfada ve sayfa üzerindeki konumlarının ne olduğunu gibi bilgileri erişmeye izin veren sınıflar sağlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.layout/
---

Bu **Aspose.Words.Layout** ad alanı, belge sayfalara biçimlendirildiğinde belirli belge öğelerinin hangi sayfada ve sayfa içinde nerede konumlandığı gibi bilgilere erişim sağlayan sınıflar sunar.

## Sınıflar

| Sınıf | Açıklama |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Bu sınıf, belge düğümlerinin sayfa numaralarını hesaplamayı sağlar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin. |
| [LayoutEnumerator](./layoutenumerator/) | Bir belgenin sayfa düzeni varlıklarını numaralandırır. Bu sınıfı sayfa düzeni modelinde dolaşmak için kullanabilirsiniz. Mevcut özellikler, varlığın render edildiği tip, geometri, metin ve sayfa indeksi ile birlikte genel yapı ve ilişkileri içerir. [GetEntity()](../) ve [Current](./layoutenumerator/get_current/) kombinasyonunu kullanarak belge düğümüne karşılık gelen varlığa geçin. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin. |
| [LayoutOptions](./layoutoptions/) | Belge düzeni sürecini kontrol etmeyi sağlayan seçenekleri tutar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin. |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Bir argüman, [Notify()](./ipagelayoutcallback/notify/) içine geçirilir. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin. |
| [RevisionOptions](./revisionoptions/) | Düzen sürecinde belge revizyonlarının nasıl ele alındığını kontrol etmeyi sağlar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin. |
## Arayüzler

| Arayüz | Açıklama |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Sayfa düzeni modelinin oluşturulması ve render edilmesi sırasında çağrılan kendi özel yönteminizi istiyorsanız bu arabirimi uygulayın. |
## Enums

| Enum | Açıklama |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Belge yorumları için render modunu belirtir. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaraları hesaplanırken farklı davranışları temsil eder. |
| [LayoutEntityType](./layoutentitytype/) | Düzen varlıklarının türleri. |
| [PageLayoutEvent](./pagelayoutevent/) | Sayfa düzeni modeli oluşturulması ve render edilmesi sırasında yükseltilen bir olay kodu. Sayfa düzeni modeli iki adımda oluşturulur. İlk olarak, "dönüştürme adımı", bu aşamada sayfa düzeni belge içeriğini çeker ve nesne grafiği oluşturur. İkinci olarak, "yeniden akış adımı", bu aşamada yapılar bölünür, birleştirilir ve sayfalara düzenlenir. Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa formatına daha fazla render edilebilir ya da edilmeyebilir. Örneğin, belgedeki sayfa sayısını hesaplamak veya alanları güncellemek render gerektirmez, ancak PDF'ye dışa aktarma gerektirir. |
| [RevisionColor](./revisioncolor/) | Belge revizyonlarının rengini belirtmeyi sağlar. |
| [RevisionTextEffect](./revisiontexteffect/) | Belge metni revizyonları için süsleme etkisini belirtmeyi sağlar. |
| [ShowInBalloons](./showinballoons/) | Balonlarda hangi revizyonların render edileceğini belirtir. |
