---
title: "Post: Business Process Model and Notation"
categories:
  - Blog
tags:
  - bpmn
  - workflow
  - bpmn-engine
---

__Related to [*workflow*](https://vhidvz.github.io/projects/project-workflow) project.__

# What's workflow?

A workflow is a sequence of steps or tasks that are performed to accomplish a specific goal or objective. Workflows can be found in many different areas of life, from business processes to software development to personal task management.

# What's BPMN?

BPMN 2 (Business Process Model and Notation 2) is a graphical notation standard for modeling business processes and workflows. It provides a standardized way to visually represent complex workflows, making them easier to understand, communicate, and automate.

BPMN 2 is maintained by the Object Management Group (OMG), an international standards organization that develops and maintains standards for modeling and managing software systems. BPMN 2 is the latest version of the BPMN standard, and it includes a wide range of features and symbols for modeling different types of workflows.

BPMN 2 uses a graphical notation to represent workflows, with different shapes and symbols representing different types of activities, events, gateways, and flows. For example, tasks are represented by rectangles, events are represented by circles, and gateways are represented by diamonds.

BPMN 2 is widely used in the software industry to model and automate business processes, especially in areas such as business process management (BPM), workflow automation, and enterprise resource planning (ERP). It can be used to model both simple and complex workflows, and it provides a standardized way to communicate and share process models between different stakeholders, including developers, business analysts, and managers.

# What's BPMN Engine?

A BPMN (Business Process Model and Notation) engine is a software component that is designed to execute BPMN process models. It is essentially a runtime environment for running BPMN workflows and managing the execution of the various activities and tasks within the workflow.

A BPMN engine typically includes several components, such as a process engine, a rules engine, and a task engine. The process engine is responsible for interpreting and executing the BPMN process models, while the rules engine is used to evaluate business rules and decision tables. The task engine manages the execution of the various tasks and activities within the workflow, such as sending notifications, generating reports, or invoking external services.

BPMN engines are typically used to automate business processes, such as order processing, customer onboarding, or financial reporting. They can also be used to automate workflows in other areas, such as software development, project management, or human resources.

# What's the difference between BPMN and BPMN Engine?

BPMN is a graphical notation standard for modeling business processes and workflows. BPMN engines are software components that are designed to execute BPMN process models.

The @vhidvz/wfjs package is a lightweight JavaScript library for building and executing workflows, which can be used to implement a workflow engine based on BPMN concepts.

The package provides a set of classes and functions that can be used to define workflows using a simple, JSON-based format. This format includes definitions of activities, transitions, and execution contexts, as well as any necessary data or variables.

The @vhidvz/wfjs library includes support for basic BPMN constructs such as parallel gateways, exclusive gateways, and activities. It also includes features such as custom events, error handling, and persistence of workflow state.

To use the package, you would typically start by defining a set of activities and transitions that make up the workflow. These activities and transitions can then be combined into a process model, which can be executed by the @vhidvz/wfjs engine.

For example, you could define a workflow that involves several activities, such as "submit order", "approve order", and "ship order", with various decision points and branches based on the outcome of each activity. You could then use the @vhidvz/wfjs library to define the process model for this workflow, and execute it using the engine.

While the @vhidvz/wfjs package does not include all the features of a full-fledged BPMN engine, it provides a lightweight and flexible solution for implementing workflow engines in JavaScript-based applications.
