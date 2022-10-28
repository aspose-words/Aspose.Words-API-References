---
title: NodeChangingAction
second_title: Aspose.Words for C++ API Reference
description: Specifies the type of node change.
type: docs
weight: 1301
url: /cpp/aspose.words/nodechangingaction/
---
## NodeChangingAction enum


Specifies the type of node change.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Insert | 0 | A node is being inserted in the tree. |
| Remove | 1 | A node is being removed from the tree. |


## Examples




Shows how to use a NodeChangingCallback to monitor changes to the document tree in real-time as we edit it. 
```cpp
void NodeChangingCallback()
{
    auto doc = MakeObject<Document>();
    doc->set_NodeChangingCallback(MakeObject<ExNode::NodeChangingPrinter>());

    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->Writeln(u"Hello world!");
    builder->StartTable();
    builder->InsertCell();
    builder->Write(u"Cell 1");
    builder->InsertCell();
    builder->Write(u"Cell 2");
    builder->EndTable();

    builder->InsertImage(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"));

    builder->get_CurrentParagraph()->get_ParentNode()->RemoveAllChildren();
}

class NodeChangingPrinter : public INodeChangingCallback
{
private:
    void NodeInserting(SharedPtr<NodeChangingArgs> args) override
    {
        ASSERT_EQ(NodeChangingAction::Insert, args->get_Action());
        ASPOSE_ASSERT_EQ(nullptr, args->get_OldParent());
    }

    void NodeInserted(SharedPtr<NodeChangingArgs> args) override
    {
        ASSERT_EQ(NodeChangingAction::Insert, args->get_Action());
        ASSERT_FALSE(args->get_NewParent() == nullptr);

        std::cout << "Inserted node:" << std::endl;
        std::cout << String::Format(u"\tType:\t{0}", args->get_Node()->get_NodeType()) << std::endl;

        if (args->get_Node()->GetText().Trim() != u"")
        {
            std::cout << "\tText:\t\"" << args->get_Node()->GetText().Trim() << "\"" << std::endl;
        }

        std::cout << "\tHash:\t" << System::ObjectExt::GetHashCode(args->get_Node()) << std::endl;
        std::cout << String::Format(u"\tParent:\t{0} ({1})", args->get_NewParent()->get_NodeType(), System::ObjectExt::GetHashCode(args->get_NewParent()))
                  << std::endl;
    }

    void NodeRemoving(SharedPtr<NodeChangingArgs> args) override
    {
        ASSERT_EQ(NodeChangingAction::Remove, args->get_Action());
    }

    void NodeRemoved(SharedPtr<NodeChangingArgs> args) override
    {
        ASSERT_EQ(NodeChangingAction::Remove, args->get_Action());
        ASSERT_TRUE(args->get_NewParent() == nullptr);

        std::cout << String::Format(u"Removed node: {0} ({1})", args->get_Node()->get_NodeType(), System::ObjectExt::GetHashCode(args->get_Node()))
                  << std::endl;
    }
};
```

