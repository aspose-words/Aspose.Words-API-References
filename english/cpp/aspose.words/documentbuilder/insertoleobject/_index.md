---
title: InsertOleObject
second_title: Aspose.Words for C++ API Reference
description: Inserts an embedded OLE object from a stream into the document.
type: docs
weight: 521
url: /cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded OLE object from a stream into the document.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream containing application data. |
| progId | const System::String\& | Programmatic Identifier of OLE object. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| progId | const System::String\& | ProgId of OLE object. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
