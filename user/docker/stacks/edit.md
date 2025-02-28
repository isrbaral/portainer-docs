# Inspect or edit a stack

## Inspecting a stack

From the menu select **Stacks** then select the stack you want to inspect.

<figure><img src="../../../.gitbook/assets/2.15-docker_inspect_stack.gif" alt=""><figcaption></figcaption></figure>

From here you can stop, delete or [create a template from the stack](template.md), and if deployed from Git you can [detach the stack from the Git repository](edit.md#detach-from-git).

<figure><img src="../../../.gitbook/assets/2.15-docker_inspect_stack_details_wp.png" alt=""><figcaption></figcaption></figure>

If the stack was deployed from a Git repository, you can:

* Configure [automatic updates](add.md#automatic-updates) or manually pull and redeploy the stack.
* View and edit the stack's environment variables.

<figure><img src="../../../.gitbook/assets/2.15-docker_inspect_redeploy_git_repo.png" alt=""><figcaption></figcaption></figure>

If the stack was deployed using the [Web Editor](add.md#option-1-web-editor) or [uploaded](add.md#option-2-upload), you will have the option to [edit your compose file manually](edit.md#editing-a-stack).

Regardless of the deployment method used, you can also [migrate or duplicate](migrate.md) the stack.

### Docker Standalone

When using Docker Standalone, you can:

* View the containers that make up the stack.
* Check to see if they are running or stopped.
* Get access to logs.
* Inspect individual containers.
* View container statistics.
* Get access to the container's console.

<figure><img src="../../../.gitbook/assets/2.15-docker_inspect_view_standalone_containers.png" alt=""><figcaption></figcaption></figure>

### Docker Swarm

When using Docker Swarm, you can:

* View the services that make up the stack.
* Check to see if they are running or stopped.
* See how many replicas are running on each host.
* Get access to logs.
* Inspect individual services.
* View service statistics.
* Get access to the service's console.

<figure><img src="../../../.gitbook/assets/2.15-docker_inspect_view_swarm_services.png" alt=""><figcaption></figcaption></figure>

## Editing a stack

Editing a stack allows you to make changes to the configuration and redeploy those changes. To edit a stack, from the menu select **Stacks**, select the stack you want to edit, then select the **Editor** tab.

{% hint style="info" %}
The Editor tab is only available for stacks that were deployed using the [Web Editor](add.md#option-1-web-editor). For stacks deployed from a Git repository, the docker-compose file must be edited in the repository itself.
{% endhint %}

<figure><img src="../../../.gitbook/assets/2.15-docker_editing_stack_editor.png" alt=""><figcaption></figcaption></figure>

Here, you can edit the Compose file for the stack to suit your needs, as well as toggle the stack [webhook](webhooks.md) and retrieve the webhook URL. You can also make changes to environment variables for the stack, and on Docker Swarm environments you can prune services if you have made changes that remove some services from the stack.

{% hint style="info" %}
You can search within the web editor at any time by pressing `Ctrl-F` (or `Cmd-F` on Mac).
{% endhint %}

When you have finished making changes, click **Update the stack**.

## Detach from Git

If your stack was created from a Git repository, you have the option to detach the stack from the repository. This means you can [edit the stack directly within Portainer](edit.md#editing-a-stack), but it does mean that the stack can't be updated from Git anymore. This action also cannot be reversed.

{% hint style="info" %}
Detaching downloads the main compose file for the stack and stores it in Portainer. It does not download any additional compose files or `.env` files that may be contained within the repository.
{% endhint %}

Click **Detach from Git** to detach. You will be asked to confirm the action - click **Detach** to do so.
