# How to Create Custom Mask Patterns in .NET MAUI SfMaskedEntry

The `CustomCharacters` property provides built-in support for creating custom mask patterns, allowing you to define your own masking rules based on application requirements.

To create a custom mask pattern, define the custom characters and use them within the `Mask` property:

* The `CustomCharacters` property allows you to associate a mask symbol with a specific validation rule.
* The `Mask` property uses the custom symbols to enforce the desired input pattern.
* Users can enter data only when it matches the rules defined for the custom mask characters.

This approach enables flexible input handling while ensuring that data is entered in the required format.

### Benefits of Using Custom Mask Patterns

* Supports application-specific input requirements.
* Provides greater flexibility than standard mask characters.
* Improves data accuracy and consistency.
* Simplifies validation for unique formats.
* Enhances the user experience with guided data entry.

## Example Scenario

Consider an input field that for custom order ID pattern that combines uppercase letters, digits, and literal separators to enforce a structured identifier

**MainPage.xaml**
```
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:editors="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"
             x:Class="MaskedEntrySample.MainPage">
    
    <VerticalStackLayout>
        <editors:SfMaskedEntry x:Name="productKeyEntry"
                       Placeholder="Enter order ID"
                       ClearButtonVisibility="WhileEditing"
                       MaskType="Simple"
                       Mask="ORD-00000-LL"
                       PromptChar="#"/>
    </VerticalStackLayout>
</ContentPage>
```
