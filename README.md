# Canvas App Hub Suite
## Summary
This project leverages the Power Platform technology to develop a customizable Multiple Canvas Apps Demo solution. The goal of the solution is to provide a comprehensive template that Partners and Customers can use as a "getting started" kit for building and publishing new solutions.

The solution will include a main hub app and multiple child canvas apps that can be easily customized and adapted to meet the needs of different industries and use cases. The solution will be designed to be intuitive, user-friendly, and easy to navigate, with a focus on streamlining the development and deployment process for Partners and Customers. 

By providing a standardized framework for building and publishing large Canvas App solutions, this project aims to facilitate greater collaboration, innovation, and growth within the Power Platform community.

## Features
This template solution will cover some common development practice.
* How to structure Component Library in your multi–App Solution 
* How to design a Main Hub App and Child Apps effectively
* How to wrap multiple canvas apps together as a single mobile app package [Overview of wrap - Power Apps | Microsoft Learn](https://learn.microsoft.com/en-us/power-apps/maker/common/wrap/overview) (Optional)

## High level structure
![App Structure](/images/CanvasAppHubSuiteSummary.png)

## Demo
<img src="images/ContosoMainHubDemo.gif?raw=true" width=60% height=60%>

## Component Details
Dataverse Key Table:

*  **App** table holds app data for each tile in the Main Menu. To launch a canvas app from another canvas app, we need the App GUID. However, for Model Driven App or other locations, we can simply use the full URL.

Note: You can use Model Driven App **Admin App** to control the value of each row in **App** table.

Component Libaries:

* **Contoso App Library** is a library of reusable components that can be shared among multiple apps, such as headers, footers, app menus, footer menus, search boxes, and loading screens.

Canvas App:

* **Contoso Main App Hub** acts as a "home base" for users, allowing them to launch different apps/url(s), access data, and perform a range of tasks, all within the same interface.
* **Contoso Product App** is a sample child app that showcases Contoso's range of products in a mixed reality (MR) environment. The app provides users with a fully immersive and interactive experience, allowing them to view and interact with Contoso's products in a virtual space.
* **Contoso Leave Request App** is a sample child app that streamlines the leave request process for employees. Employees can submit leave requests, view their leave balance, and track the status of their requests.
* **Contoso Feeds App**is a sample child app that displays the latest and most important news from multiple RSS sources and presents them in an easy-to-read format.
* **Contoso Document Management App**: This is a sample child app that shows documents from a SharePoint site. The app makes it easy for users to view and manage documents, streamlining the document management process. 


Power Automate Flow:

* **Admin | Update Canvas App ID for App Menu Table in the current environment**: 
If you move the solution from one environment to another, or if you deploy it for the first time, this flow will update the App GUID with the correct GUID for the current environment.