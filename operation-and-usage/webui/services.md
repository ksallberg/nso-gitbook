---
description: Create and manage service deployment.
---

# Services

The **Services** view is used to view, create, and manage services in your NSO deployment. The default **Services** view displays the existing services.

<figure><img src="../../images/service-view.png" alt=""><figcaption><p>Services View</p></figcaption></figure>

## Search <a href="#d5e6128" id="d5e6128"></a>

If you have several services configured, you can use the **Search** to filter down results to the service of your choice. The search filter matches the entered characters to the service name and shows the results accordingly. Results are shown only for the service point that you have selected.

To filter the service list:

1. In the **Select service type** drop-down, select the service point to populate all the services under it.
2. Enter a partial or full name of the service you are searching for.
3. Press **Enter**.

## Create a Service <a href="#d5e6142" id="d5e6142"></a>

To create and deploy a service:

1. In the **Select service type** drop-down, select the service point.
2. Click the **Add service** button. You will be redirected to the **Configuration editor** view.
3. Click the plus <img src="../../images/add-action.png" alt="" data-size="line"> button.
4. In the **Add new list item** pop-up, enter the required information, which in this case is the name of the service.
5. Confirm the intent.
6. Configure additional service data in the **Configuration editor** view.
7. Review and commit the service to NSO in the **Commit manager**. Committing the service deploys it to NSO and displays it in the **Services** view.

## Edit Service Configuration <a href="#d5e6291" id="d5e6291"></a>

Service configuration is viewed and carried out in the Configuration Editor. In the **Services** view, you can use the **Modify in Config Editor** option on the desired service to access its config in the Configuration Editor.

{% hint style="warning" %}
The **Configuration editor** view shows a host of options when configuring a service. You are expected to be well-versed with these options (and service concepts in general) before you delve into service configuration. Refer to the [Services](../../development/core-concepts/services.md) and [Developing Services](../../development/advanced-development/developing-services/) documentation for more information.
{% endhint %}

To rename a service:

1. Navigate to the service using the Configuration Editor and access the **Edit config** tab.
2. Select the service in the list using the checkbox.
3. Click the pencil icon.
4. Rename the service in the pop-up.
5. Commit the change in the **Commit manager**.

To edit service configuration:

1. Navigate to the service using the Configuration Editor and access the **Edit config** tab.
2. Click the service name in the list.
3. Make the changes.
4. Commit the changes in the **Commit manager**.

{% hint style="info" %}
The other two tabs, i.e., **Config** and **Operdata** can be used respectively to view the service configuration and operational data.
{% endhint %}

## Apply an Action on a Service <a href="#d5e6164" id="d5e6164"></a>

You can apply actions on a service from the **Services** view or the **Configuration editor**.

Start by selecting the service point to populate all services under it and then follow the instructions below:

{% tabs %}
{% tab title="From the Services View" %}
To apply an action on a service:

1. On the desired service in the list, click the more options <img src="../../images/more-options.png" alt="" data-size="line"> button.
2. Choose the preferred action from the list, i.e., **Re-deploy**, **Un-deploy**, **Check sync**, **Deep check sync**, or **get modifications**.

{% hint style="info" %}
The **Check sync** action can be run on multiple services at once by selecting them using the checkbox and then running the action using the **Choose actions** button.
{% endhint %}

**Actions Possible in the Services View**

Available actions include **Re-deploy**, **Un-deploy**, **Check sync**, **Deep check sync**, and **get modifications**. See [Lifecycle Operations](../operations/lifecycle-operations.md) for the details of these actions.

{% hint style="info" %}
The **Modify in Config Editor** and **Delete** are GUI-specific operations accessible on the service row.
{% endhint %}
{% endtab %}

{% tab title="From the Configuration Editor -> Actions Tab" %}
Additional actions are applied to an individual service. Use this option if you want to run an action with additional parameters.

1. Access the service in the Configuration Editor. This you can do by selecting the **Modify in Config Editor** option in the **Services** view.
2. Access the **Actions** tab in the **Configuration editor** view.
3. Click the desired action in the list.
4.  At this point, you can configure different parameters.

    (Use the **Reset action parameters** option to reset all parameters to default value).
5. Run the action.

{% hint style="info" %}
Fetch the action information by clicking the info <img src="../../images/actions-info.png" alt="" data-size="line"> icon in the **Configuration editor** -> **Actions** tab.
{% endhint %}

**Actions Possible in the Configuration Editor -> Actions Tab**

Access the service in the **Configuration editor** to run the following actions: **check-sync**, **reactive-re-deploy**, **un-deploy**, **deep-check-sync**, **touch**, **set-rank**, **re-deploy**, **get-modifications**, and **purge.** See [Lifecycle Operations](../operations/lifecycle-operations.md) for the details of these actions.
{% endtab %}
{% endtabs %}

## View Service Details

To view details of a service:

1. In the **Select service type** drop-down, select the service point.
2. Click the desired service. This opens up the service details view.
3. Browse service details using the following tabs:
   * **Details**
   * **Plan**
   * **Log**

## Delete a Service <a href="#d5e6324" id="d5e6324"></a>

To delete a service instance:

1. In the **Select service type** drop-down list, select the service point.
2. Select, using the checkbox, the service to be deleted. You can select multiple services at once.
3. Click **Delete**.
4. Confirm the intent in the pop-up.
5. Review and commit the change in the **Commit manager**.

{% hint style="info" %}
To skip the Commit Manager review, use the **Commit changes directly** option in the **Delete service instance** pop-up.
{% endhint %}
