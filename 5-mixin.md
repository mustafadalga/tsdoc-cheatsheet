### @mixin


```typescript
/**
 * @mixin
 * Mixin named `isLoadedBillingInformation` for checking the loading state of billing information.
 *
 * @remarks
 * Use the `@mixin` tag to indicate that this object mixes in methods, properties, or other characteristics.
 * This is commonly used in Vue.js to share functionality across multiple components. In this case,
 * `isLoadedBillingInformation` is a mixin that provides a computed property to determine whether
 * billing information has been loaded. The `...mapGetters('common', ['getApisLoadStates'])` line
 * uses the `mapGetters` helper from Vuex to map the `getApisLoadStates` getter from the 'common'
 * module to a local computed property.
 */
const isLoadedBillingInformation = {
        computed: {
            ...mapGetters('common', ['getApisLoadStates']),
            /**
             * Gets the loading state of billing information.
             *
             * @returns {boolean} Whether the billing information is loaded or not.
             */
            isLoadedBillingInformation() {
                return this.getApisLoadStates.billingInformation?.isLoaded;
            },
        }
    };

```


[Back to Table of Contents](README.md)
