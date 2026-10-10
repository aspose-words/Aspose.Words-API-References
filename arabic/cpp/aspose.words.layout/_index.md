---
title: "مساحة الأسماء Aspose::Words::Layout"
linktitle: "Aspose::Words::Layout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "مساحة الأnamespaces Aspose::Words::Layout. توفر مساحة الأسماء Aspose.Words.Layout فئات تسمح بالوصول إلى معلومات مثل الصفحة التي يقع فيها وعن موقع عنصر معين من المستند على الصفحة، عندما يتم تنسيق المستند إلى صفحات في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.layout/
---

توفر مساحة الاسم **Aspose.Words.Layout** فئات تتيح الوصول إلى معلومات مثل الصفحة التي يتواجد فيها عنصر المستند وموقعه على الصفحة عندما يتم تنسيق المستند إلى صفحات.

## الفئات

| الفئة | الوصف |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | تسمح هذه الفئة بحساب أرقام الصفحات لعقد المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | يسرد كيانات تخطيط الصفحة لمستند. يمكنك استخدام هذه الفئة للتجول في نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع، الهندسة، النص وفهرس الصفحة حيث يتم عرض الكيان، بالإضافة إلى الهيكل العام والعلاقات. استخدم الجمع بين [GetEntity()](../) و[Current](./layoutenumerator/get_current/) للانتقال إلى الكيان الذي يتطابق مع عقدة المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | يحتوي على الخيارات التي تسمح بالتحكم في عملية تخطيط المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | معامل يُمرَّر إلى [Notify()](./ipagelayoutcallback/notify/). لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | يسمح بالتحكم في كيفية معالجة مراجعات المستند أثناء عملية التخطيط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## الواجهات

| الواجهة | الوصف |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقة مخصصة تُستدعى أثناء بناء وعرض نموذج تخطيط الصفحة. |
## Enums

| Enum | الوصف |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | يحدد وضعية العرض لتعليقات المستند. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد بدء ترقيم الصفحات. |
| [LayoutEntityType](./layoutentitytype/) | أنواع كيانات التخطيط. |
| [PageLayoutEvent](./pagelayoutevent/) | رمز الحدث الذي يُرفع أثناء بناء وعرض نموذج تخطيط الصفحة. يتم بناء نموذج تخطيط الصفحة على خطوتين. الأولى، "خطوة التحويل"، وهي عندما يسحب تخطيط الصفحة محتوى المستند وينشئ رسمًا بيانيًا للكائنات. الثانية، "خطوة إعادة التدفق"، وهي عندما يتم تقسيم الهياكل ودمجها وترتيبها في صفحات. اعتمادًا على العملية التي أدت إلى البناء، قد يتم أو لا يتم عرض نموذج تخطيط الصفحة لاحقًا إلى تنسيق صفحة ثابتة. على سبيل المثال، حساب عدد الصفحات في المستند أو تحديث الحقول لا يتطلب عرضًا، بينما تصدير إلى PDF يتطلب ذلك. |
| [RevisionColor](./revisioncolor/) | يسمح بتحديد لون مراجعات المستند. |
| [RevisionTextEffect](./revisiontexteffect/) | يسمح بتحديد تأثير الزخرفة لمراجعات نص المستند. |
| [ShowInBalloons](./showinballoons/) | يحدد أي المراجعات تُعرض في الفقاعات. |
