---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::PageLayoutEvent enum. Sayfa düzeni modeli oluşturulurken ve render edilirken tetiklenen bir olay kodu. Sayfa düzeni modeli iki adımda oluşturulur. İlk olarak, \"conversion step\" (dönüştürme adımı), bu adımda sayfa düzeni belge içeriğini çeker ve nesne grafiği oluşturur. İkinci olarak, \"reflow step\" (yeniden akış adımı), bu adımda yapılar bölünür, birleştirilir ve sayfalara düzenlenir. Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa formatına daha fazla render edilebilir veya edilmeyebilir. Örneğin, belgede sayfa sayısını hesaplamak veya alanları güncellemek render gerektirmez, ancak PDF'ye dışa aktarma C++'ta bunu gerektirir."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


Sayfa düzeni modeli oluşturulması ve render edilmesi sırasında yükseltilen bir olay kodu. Sayfa düzeni modeli iki adımda oluşturulur. İlk olarak, "dönüştürme adımı", bu aşamada sayfa düzeni belge içeriğini çeker ve nesne grafiği oluşturur. İkinci olarak, "yeniden akış adımı", bu aşamada yapılar bölünür, birleştirilir ve sayfalara düzenlenir. Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa formatına daha fazla render edilebilir ya da edilmeyebilir. Örneğin, belgedeki sayfa sayısını hesaplamak veya alanları güncellemek render gerektirmez, ancak PDF'ye dışa aktarma gerektirir.

```cpp
enum class PageLayoutEvent
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Varsayılan değer. |
| WatchDog | 1 | Genellikle ziyaret edilen ve işlemi iptal etmeye uygun bir kod noktasına karşılık gelir. [Notify()](../ipagelayoutcallback/notify/) içinde, işlemi iptal etmek için özel bir istisna fırlatın. Herhangi bir geri çağırma olayını işlerken işlemi iptal etmek için fırlatabilirsiniz. İşlem iptal edilirse sayfa düzeni modeli tanımsız bir durumda kalır. Ancak, tam bir sayfanın yeniden akışı sırasında işlem iptal edilirse, o sayfanın sonuna kadar düzen modeli kullanılabilir olmalıdır. |
| BuildStarted | 2 | Sayfa düzeni oluşturulması başladı. Bir kez tetiklenir. Bu, [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) çağrıldığında gerçekleşen ilk olaydır. |
| BuildFinished | 3 | Sayfa düzeni oluşturulması tamamlandı. Bir kez tetiklenir. Bu, [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) çağrıldığında gerçekleşen son olaydır. |
| ConversionStarted | 4 | Belge modelinin sayfa düzenine dönüştürülmesi başladı. Bir kez tetiklenir. Bu, düzen modeli belge içeriğini çekmeye başladığında gerçekleşir. |
| ConversionFinished | 5 | Belge modelinin sayfa düzenine dönüştürülmesi tamamlandı. Bir kez tetiklenir. Bu, düzen modeli belge içeriğini çekmeyi durdurduğunda gerçekleşir. |
| ReflowStarted | 6 | Sayfa düzeninin yeniden akışı başladı. Bir kez tetiklenir. Bu, düzen modeli belge içeriğini yeniden akıtmaya başladığında gerçekleşir. |
| ReflowFinished | 7 | Sayfa düzeninin yeniden akışı tamamlandı. Bir kez tetiklenir. Bu, düzen modeli belge içeriğini yeniden akıtmayı durdurduğunda gerçekleşir. |
| PartReflowStarted | 8 | Sayfanın yeniden akışı başladı. Sayfanın birden fazla kez yeniden akışa girebileceğini ve yeniden akışın tamamlanmadan önce yeniden başlayabileceğini unutmayın. |
| PartReflowFinished | 9 | Sayfanın yeniden akışı tamamlandı. Sayfanın birden fazla kez yeniden akışa girebileceğini ve yeniden akışın tamamlanmadan önce yeniden başlayabileceğini unutmayın. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) sayfasının render edilmesi başladı. Bu, sayfa başına bir kez tetiklenir. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) sayfasının render edilmesi tamamlandı. Bu, sayfa başına bir kez tetiklenir. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
