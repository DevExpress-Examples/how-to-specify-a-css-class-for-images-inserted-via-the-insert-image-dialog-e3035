<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/Default.aspx) (VB: [Default.aspx](./VB/Default.aspx))
* [Default.aspx.cs](./CS/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/Default.aspx.vb))
* [ImagePropertiesForm.ascx](./CS/DevExpress/ASPxHtmlEditorForms/ImagePropertiesForm.ascx) (VB: [ImagePropertiesForm.ascx](./VB/DevExpress/ASPxHtmlEditorForms/ImagePropertiesForm.ascx))
* [ImagePropertiesForm.ascx.cs](./CS/DevExpress/ASPxHtmlEditorForms/ImagePropertiesForm.ascx.cs) (VB: [ImagePropertiesForm.ascx.vb](./VB/DevExpress/ASPxHtmlEditorForms/ImagePropertiesForm.ascx.vb))
* [InsertImageForm.ascx](./CS/DevExpress/ASPxHtmlEditorForms/InsertImageForm.ascx) (VB: [InsertImageForm.ascx](./VB/DevExpress/ASPxHtmlEditorForms/InsertImageForm.ascx))
* [InsertImageForm.ascx.cs](./CS/DevExpress/ASPxHtmlEditorForms/InsertImageForm.ascx.cs) (VB: [InsertImageForm.ascx.vb](./VB/DevExpress/ASPxHtmlEditorForms/InsertImageForm.ascx.vb))
* [SelectImageForm.ascx](./CS/DevExpress/ASPxHtmlEditorForms/SelectImageForm.ascx) (VB: [SelectImageForm.ascx](./VB/DevExpress/ASPxHtmlEditorForms/SelectImageForm.ascx))
* [SelectImageForm.ascx.cs](./CS/DevExpress/ASPxHtmlEditorForms/SelectImageForm.ascx.cs) (VB: [SelectImageForm.ascx.vb](./VB/DevExpress/ASPxHtmlEditorForms/SelectImageForm.ascx.vb))
<!-- default file list end -->
# How to specify a CSS class for images inserted via the Insert Image dialog
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e3035)**
<!-- run online end -->


<p>From v2010 vol 2.6 you can specify the CSS class for images inserted via the Insert Image dialog.  For this purpose the <strong>cssClass</strong> field has been added to the <strong>GetDialogData_InsertImageForm</strong> function within the InsertImageForm.ascx file.<br />
This example demonstrates how to:<br />
- specify a CSS class for the inserted image;<br />
- specify a .css document for an ASPxHtmlEditor;<br />
- customize a default dialog.</p><p>Default dialog forms have been copied to the web project for further modification (for details, see <a href="http://documentation.devexpress.com/#AspNet/CustomDocument8904"><u>Customization of Default Dialog Forms</u></a>). The ASPxLabel control and ASPxComboBox controls have been added to the ImagePropertiesForm.ascx file markup. The combo box contains tree items specifying names of CSS classes. The <strong>GetDialogData_InsertImageForm</strong> function has been modified to get the selected CSS class name from the combo box. The image gets CSS class settings from the file, specified via <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxHtmlEditorHtmlEditorCssFile_FilePathtopic"><u>FilePath</u></a> property (Document.css in our case).</p><p>The image below shows the result:<br />
<img src="https://raw.githubusercontent.com/DevExpress-Examples/how-to-specify-a-css-class-for-images-inserted-via-the-insert-image-dialog-e3035/13.1.12+/media/c5151936-521f-4c5e-b2fa-825d2b0ffda3.png"><br />
<strong>Note</strong></p><p>Starting from version 2013.2, image dialogs provide an ability to specify an image CSS class without copying the dialog form to the project. Set the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxHtmlEditorHtmlEditorInsertImageDialogSettings_ShowImageStyleSettingsSectiontopic"><u>ShowImageStyleSettingsSection</u></a> property to <strong>true</strong> to display the image style settings, which include margins, a border and CSS class, in the <strong>More options</strong> section. You can see this feature in the <a href="http://demos.devexpress.com/ASPxHTMLEditorDemos/ToolbarItems/CustomCSS.aspx"><u>Custom CSS</u></a> demo.</p>

<br/>


