# How to add custom button in toolbar

The toolbar items can be customized using the [toolbarSettings](../../api/file-manager/#toolbarsettings) API and [toolbarClick](../../api/file-manager/#toolbarclick) events.

The following example shows adding a custom item in the toolbar.

The new toolbar button is added using [toolbarSettings](../../api/file-manager/#toolbarsettings). The [toolbarClick](../../api/file-manager/#toolbarclick) event is used to add an event handler to the new toolbar button.

{% tab template="file-manager/toolbar", compileJsx=true, sourceFiles="app/App.tsx,app/index.tsx,index.html" %}

{% endtab %}