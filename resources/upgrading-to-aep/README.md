# Upgrade to the Experience Platform SDKs

This section contains a checklist that you can use as you plan your upgrade to the Experience Platform SDKs.

{% hint style="danger" %}
The Experience Platform SDK contains **breaking changes** from the 4x SDKs.   
  
In addition to changed APIs, the new SDK includes new APIs and deprecation of APIs such as timed action and milestone media video tracking.
{% endhint %}

### Important considerations

The Experience Platform SDK have been significantly architecturally re-designed, which changes how customers implement and leverage the SDKs. Review the following checklist to understand some of the changes and what is required to upgrade:

1. The Experience Platform SDKs introduce the [Mobile Core](../../using-mobile-extensions/mobile-core/) and constituent extensions.  Mobile Core contains core SDK functionality that is required for all implementations that require Adobe and/or third-party extensions.
2. The Mobile Core and other extensions are configured in Launch in a mobile property.  When published, Launch hosts this property configuration and makes it for your SDK implementation.
3. You decide which SDK extensions to add, configure, and ultimately include in your app project. This provides the flexibility to customize your implementations.  **Important**: Some extensions depend on others for proper functioning, and these are documented where applicable.
4. We recommend that you ease your build process by use supported dependency managers, such as Gradle for Android and Cocoapods for iOS.  Launch provides inline instructions and specs to help you with this process. 

## Upgrade checklist

1. Begin with [Getting Started](../../getting-started/create-a-mobile-property.md) section and ensure that you are appropriately provisioned for Launch.
2. Ensure all of the required SDK APIs that you currently use are available in the new SDK. For more information, see [Experience Platform SDKs vs. the 4x SDK](aepvs4x.md)s. **Tip**: The Experience Platform SDK supports iOS versions 10+, Android 4+ \(API 14+\).
3. If you are implementing Analytics, see [Processing rules overview](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules.html) to map the variables and rules.

{% hint style="success" %}
The Experience Platform SDK automatically performs migration tasks that are required to preserve locally stored user context. Without manual intervention, you should expect no change to your visitor reporting or marketing campaigns.
{% endhint %}

{% hint style="info" %}
This client-side, SDK upgrade does not affect marketing campaigns that are in progress, reporting, or other app activities that are configured in Experience Cloud solutions.
{% endhint %}

## Further reading

* See [Experience Cloud vs. 4x SDK functionality comparison](aepvs4x.md) 
* Visit and ask questions on our [community forum](https://forums.adobe.com/community/experience-cloud/platform/launch/sdk) to get quick, thorough responses

