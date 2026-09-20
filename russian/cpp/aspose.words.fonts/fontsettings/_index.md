---
title: "Aspose::Words::Fonts::FontSettings class"
linktitle: "FontSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSettings class. Указывает параметры шрифтов для документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.fonts/fontsettings/
---
## FontSettings class


Указывает настройки шрифта для документа. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSettings : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [FontSettings](./fontsettings/)() |  |
| static [get_DefaultInstance](./get_defaultinstance/)() | Статические параметры шрифтов по умолчанию. |
| [get_FallbackSettings](./get_fallbacksettings/)() const | [Настройки](../../aspose.words.settings/) связанные с механизмом подстановки шрифтов. |
| [get_SubstitutionSettings](./get_substitutionsettings/)() const | [Настройки](../../aspose.words.settings/) связанные с механизмом замены шрифтов. |
| [GetFontsSources](./getfontssources/)() | Получает копию массива, содержащего список источников, где Aspose.Words ищет шрифты TrueType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ResetFontSources](./resetfontsources/)() | Сбрасывает источники шрифтов к системным настройкам по умолчанию. |
| [SaveSearchCache](./savesearchcache/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сохраняет кэш поиска шрифтов в поток. |
| [SetFontsFolder](./setfontsfolder/)(const System::String\&, bool) | Устанавливает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. Это ярлык к [SetFontsFolders()](../) для указания только одного каталога шрифтов. |
| [SetFontsFolders](./setfontsfolders/)(const System::ArrayPtr\<System::String\>\&, bool) | Устанавливает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) | Устанавливает источники, где Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Устанавливает источники, где Aspose.Words ищет шрифты TrueType, и дополнительно загружает ранее сохранённый кэш поиска шрифтов. |
| static [Type](./type/)() |  |
## Примечания


Aspose.Words использует параметры шрифтов для разрешения шрифтов в документе. [Fonts](../) в основном разрешаются при построении макета документа или рендеринге в фиксированные форматы страниц. Но при загрузке некоторых форматов Aspose.Words также может потребоваться разрешить шрифты. Например, при загрузке HTML‑документов Aspose.Words может разрешать шрифты для выполнения подстановки шрифтов. Поэтому рекомендуется установить параметры шрифтов в [LoadOptions](../../aspose.words.loading/loadoptions/) при загрузке документа. Или, как минимум, перед построением макета или рендерингом документа в фиксированный формат страницы.

По умолчанию все документы используют единственный статический экземпляр настроек шрифтов. К нему можно получить доступ через свойство [DefaultInstance](./get_defaultinstance/).

Изменение настроек шрифтов безопасно в любое время из любого потока. Однако рекомендуется не менять настройки шрифтов во время обработки некоторых документов, которые используют эти настройки. Это может привести к тому, что один и тот же шрифт будет определяться по‑разному в разных частях документа.

## Примеры



Показывает, как задать каталог источника шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифтов при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// В стандартных источниках шрифтов отсутствуют два шрифта, которые мы используем в этом документе.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Используйте метод "SetFontsFolder", чтобы задать каталог, который будет выступать новым источником шрифтов.
// Передайте "false" в качестве аргумента "recursive", чтобы включить шрифты из всех файлов шрифтов, находящихся в каталоге
// который мы передаём в первом аргументе, но не включать шрифты из подпапок этого каталога.
// Передайте "true" в качестве аргумента "recursive", чтобы включить все файлы шрифтов в каталоге, который мы передаём
// в первом аргументе, а также все шрифты в его подпапках.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolder(get_FontsDir(), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Шрифт "Amethysta" находится в подпапке каталога шрифтов.
if (recursive)
{
    ASSERT_EQ(30, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolder.pdf");

// Восстановите оригинальные источники шрифтов.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```


Показывает, как задать несколько каталогов источников шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифтов при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// В стандартных источниках шрифтов отсутствуют два шрифта, которые мы используем в этом документе.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Используйте метод "SetFontsFolders", чтобы создать источник шрифтов из каждого каталога шрифтов, который мы передаём в качестве первого аргумента.
// Передайте "false" в качестве аргумента "recursive", чтобы включить шрифты из всех файлов шрифтов, находящихся в каталогах
// которые мы передаём в первом аргументе, но не включать шрифты из подпапок этих каталогов.
// Передайте "true" в качестве аргумента "recursive", чтобы включить все файлы шрифтов в каталогах, которые мы передаём
// в первом аргументе, а также все шрифты в их подпапках.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolders(System::MakeArray<System::String>({get_FontsDir() + u"/Amethysta", get_FontsDir() + u"/Junction"}), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Папка "Junction" сама по себе не содержит файлов шрифтов, но имеет подпапки, где они есть.
if (recursive)
{
    ASSERT_EQ(11, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Junction Light";
    }))));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolders.pdf");

// Восстановите оригинальные источники шрифтов.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```


Показывает, как добавить источник шрифтов к нашим существующим источникам шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// В стандартном источнике шрифтов отсутствуют два шрифта, которые мы используем в нашем документе.
// Когда мы сохраняем этот документ, Aspose.Words применит резервные шрифты ко всему тексту, отформатированному недоступными шрифтами.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Создайте источник шрифтов из папки, содержащей шрифты.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Примените новый массив источников шрифтов, который содержит оригинальные источники шрифтов, а также наши пользовательские шрифты.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Убедитесь, что Aspose.Words имеет доступ ко всем необходимым шрифтам перед тем, как мы рендерим документ в PDF.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// Восстановите оригинальные источники шрифтов.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
