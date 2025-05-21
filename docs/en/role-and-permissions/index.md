# Permission Inheritance

![](/images/role-and-permission/permissionInheritance.png){data-zoomable}

When you assign a role to a user at any level, those permissions are automatically **inherited** by the levels below it.

**Simple Examples:**

* If you give a user the **Admin** role at the **Platform** level, that user will also have Admin access in **Service** and **Component**.
* If you give a user **Full Control** at the **Service** level, that user will have Full Control in **Component** but will not have management rights at the **Platform** level.

**Why is this important?**

Understanding roles and permission inheritance helps you manage system access correctly and securely, ensuring everyone has the necessary permissions to do their job.