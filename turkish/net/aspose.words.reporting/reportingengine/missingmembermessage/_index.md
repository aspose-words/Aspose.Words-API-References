---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: .NET için Aspose.Words
description: ReportingEngine MissingMemberMessage özelliğini keşfedin, eksik nesne üyeleri için mesajları kolaylıkla özelleştirin. Kullanıcı deneyimini zahmetsizce geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Bir nesnenin eksik bir üyesine düz bir referansı temsil eden bir şablon ifadesi yerine yazdırılan bir dize değerini alır veya ayarlar. Varsayılan değer boş bir dizedir.

```csharp
public string MissingMemberMessage { get; set; }
```

## Notlar

Özellik, aşağıdakilerle birlikte kullanılmalıdır:AllowMissingMembers seçeneği. Aksi takdirde, bir nesnenin eksik bir üyesiyle karşılaşıldığında bir istisna atılır.

Özellik yalnızca missing nesne üyesine düz bir referansı temsil eden bir şablon ifadesinin yazdırılmasını etkiler. Örneğin, işlenenlerinden biri missing nesne üyesine referans veren ikili bir operatörün yazdırılması etkilenmez.

Bu özelliğin değeri null olarak ayarlanamaz.

## Örnekler

Eksik üyelere nasıl izin verileceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Ayrıca bakınız

* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
