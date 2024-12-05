# Angular Interview Questions & Answers

> Click :star:if you like the project and follow [@SudheerJonna](https://twitter.com/SudheerJonna) for technical updates. 

---

<p align="center">
  <a href=https://zerotomastery.io/?utm_source=github&utm_medium=sponsor&utm_campaign=angular-interview-questions>
    <img src=https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=height:70/https://www.filepicker.io/api/file/AKYtjj5SSGyJuyZrkAB2 alt="ZTM Logo" width="100" height="50">
  </a>
  <p align="center">
    <ol>
    <li>Take this <a href=https://links.zerotomastery.io/angular_sudheer>Angular course</a> to go from a complete Angular beginner to confidently building enterprise-level applications from scratch</li>
    <li>Take this <a href=https://links.zerotomastery.io/mci_sudheer3>coding interview bootcamp</a> if you’re serious about getting hired and don’t have a CS degree</li>
    </ol>
  </p>
</p>

---

### Table of Contents

| No. | Questions |
|---- | ---------
|1 | [What is Angular Framework?](#what-is-angular-framework)|
|2 | [What is the difference between AngularJS and Angular?](#what-is-the-difference-between-angularjs-and-angular)|
|3 | [What is TypeScript?](#what-is-typescript)|
|4 | [Write a pictorial diagram of Angular architecture?](#write-a-pictorial-diagram-of-angular-architecture)|
|5 | [What are the key components of Angular?](#what-are-the-key-components-of-angular)|
|6 | [What are directives?](#what-are-directives)|
|7 | [What are components?](#what-are-components)|
|8 | [What are the differences between Component and Directive?](#what-are-the-differences-between-component-and-directive)|
|9 | [What is a template?](#what-is-a-template)|
|10| [What is a module?](#what-is-a-module)|
|11| [What are lifecycle hooks available?](#what-are-lifecycle-hooks-available)|
|12| [What is a data binding?](#what-is-a-data-binding)|
|13| [What is metadata?](#what-is-metadata)|
|14| [What is Angular CLI?](#what-is-angular-cli)|
|15| [What is the difference between constructor and ngOnInit?](#what-is-the-difference-between-constructor-and-ngoninit)|
|16| [What is a service](#what-is-a-service)|
|17| [What is dependency injection in Angular?](#what-is-dependency-injection-in-angular)|
|18| [How is Dependency Hierarchy formed?](#how-is-dependency-hierarchy-formed)|
|19| [What is the purpose of async pipe?](#what-is-the-purpose-of-async-pipe)|
|20| [What is the option to choose between inline and external template file?](#what-is-the-option-to-choose-between-inline-and-external-template-file)|
|21| [What is the purpose of *ngFor directive?](#what-is-the-purpose-of-ngfor-directive)|
|22| [What is the purpose of ngIf directive?](#what-is-the-purpose-of-ngif-directive)|
|23| [What happens if you use script tag inside template?](#what-happens-if-you-use-script-tag-inside-template)|
|24| [What is interpolation?](#what-is-interpolation)|
|25| [What are template expressions?](#what-are-template-expressions)|
|26| [What are template statements?](#what-are-template-statements)|
|27| [How do you categorize data binding types?](#how-do-you-categorize-data-binding-types)|
|28| [What are pipes?](#what-are-pipes)|
|29| [What is a parameterized pipe?](#what-is-a-parameterized-pipe)|
|30| [How do you chain pipes?](#how-do-you-chain-pipes)|
|31| [What is a custom pipe?](#what-is-a-custom-pipe)|
|32| [Give an example of custom pipe?](#give-an-example-of-custom-pipe)|
|33| [What is the difference between pure and impure pipe?](#what-is-the-difference-between-pure-and-impure-pipe)|
|34| [What is a bootstrapping module?](#what-is-a-bootstrapping-module)|
|35| [What are observables?](#what-are-observables)|
|36| [What is HttpClient and its benefits?](#what-is-httpclient-and-its-benefits)|
|37| [Explain on how to use HttpClient with an example?](#explain-on-how-to-use-httpclient-with-an-example)|
|38| [How can you read full response?](#how-can-you-read-full-response)|
|39| [How do you perform Error handling?](#how-do-you-perform-error-handling)|
|40| [What is RxJS?](#what-is-rxjs)|
|41| [What is subscribing?](#what-is-subscribing)|
|42| [What is an observable?](#what-is-an-observable)|
|43| [What is an observer?](#what-is-an-observer)|
|44| [What is the difference between promise and observable?](#what-is-the-difference-between-promise-and-observable)|
|45| [What is multicasting?](#what-is-multicasting)|
|46| [How do you perform error handling in observables?](#how-do-you-perform-error-handling-in-observables)|
|47| [What is the shorthand notation for subscribe method?](#what-is-the-shorthand-notation-for-subscribe-method)|
|48| [What are the utility functions provided by RxJS?](#what-are-the-utility-functions-provided-by-rxjs)|
|49| [What are observable creation functions?](#what-are-observable-creation-functions)|
|50| [What will happen if you do not supply handler for the observer?](#what-will-happen-if-you-do-not-supply-handler-for-the-observer)|
|51| [What are Angular elements?](#what-are-angular-elements)|
|52| [What is the browser support of Angular Elements?](#what-is-the-browser-support-of-angular-elements)|
|53| [What are custom elements?](#what-are-custom-elements)|
|54| [Do I need to bootstrap custom elements?](#do-i-need-to-bootstrap-custom-elements)|
|55| [Explain how custom elements works internally?](#explain-how-custom-elements-works-internally)|
|56| [How to transfer components to custom elements?](#how-to-transfer-components-to-custom-elements)|
|57| [What are the mapping rules between Angular component and custom element?](#what-are-the-mapping-rules-between-angular-component-and-custom-element)|
|58| [How do you define typings for custom elements?](#how-do-you-define-typings-for-custom-elements)|
|59| [What are dynamic components?](#what-are-dynamic-components)|
|60| [What are the various kinds of directives?](#what-are-the-various-kinds-of-directives)|
|61| [How do you create directives using CLI?](#how-do-you-create-directives-using-cli)|
|62| [Give an example for attribute directives?](#give-an-example-for-attribute-directives)|
|63| [What is Angular Router?](#what-is-angular-router)|
|64| [What is the purpose of base href tag?](#what-is-the-purpose-of-base-href-tag)|
|65| [What are the router imports?](#what-are-the-router-imports)|
|66| [What is router outlet?](#what-is-router-outlet)|
|67| [What are router links?](#what-are-router-links)|
|68| [What are active router links?](#what-are-active-router-links)|
|69| [What is router state?](#what-is-router-state)|
|70| [What are router events?](#what-are-router-events)|
|71| [What is activated route?](#what-is-activated-route)|
|72| [How do you define routes?](#how-do-you-define-routes)|
|73| [What is the purpose of Wildcard route?](#what-is-the-purpose-of-wildcard-route)|
|74| [Do I need a Routing Module always?](#do-i-need-a-routing-module-always)|
|75| [What is Angular Universal?](#what-is-angular-universal)|
|76| [What are different types of compilation in Angular?](#what-are-different-types-of-compilation-in-angular)|
|77| [What is JIT?](#what-is-jit)|
|78| [What is AOT?](#what-is-aot)|
|79| [Why do we need compilation process?](#why-do-we-need-compilation-process)|
|80| [What are the advantages with AOT?](#what-are-the-advantages-with-aot)|
|81| [What are the ways to control AOT compilation?](#what-are-the-ways-to-control-aot-compilation)|
|82| [What are the restrictions of metadata?](#what-are-the-restrictions-of-metadata)|
|83| [What are the three phases of AOT?](#what-are-the-three-phases-of-aot)|
|84| [Can I use arrow functions in AOT?](#can-i-use-arrow-functions-in-aot)|
|85| [What is the purpose of metadata json files?](#what-is-the-purpose-of-metadata-json-files)|
|86| [Can I use any javascript feature for expression syntax in AOT?](#can-i-use-any-javascript-feature-for-expression-syntax-in-aot)|
|87| [What is folding?](#what-is-folding)|
|88| [What are macros?](#what-are-macros)|
|89| [Give an example of few metadata errors?](#give-an-example-of-few-metadata-errors)|
|90| [What is metadata rewriting?](#what-is-metadata-rewriting)|
|91| [How do you provide configuration inheritance?](#how-do-you-provide-configuration-inheritance)|
|92| [How do you specify angular template compiler options?](#how-do-you-specify-angular-template-compiler-options)|
|93| [How do you enable binding expression validation?](#how-do-you-enable-binding-expression-validation)|
|94| [What is the purpose of any type cast function?](#what-is-the-purpose-of-any-type-cast-function)|
|95| [What is Non null type assertion operator?](#what-is-non-null-type-assertion-operator)|
|96| [What is type narrowing?](#what-is-type-narrowing)|
|97| [How do you describe various dependencies in angular application?](#how-do-you-describe-various-dependencies-in-angular-application)|
|98| [What is zone?](#what-is-zone)|
|99| [What is the purpose of common module?](#what-is-the-purpose-of-common-module)|
|100| [What is codelyzer?](#what-is-codelyzer)|
|101| [What is angular animation?](#what-is-angular-animation)|
|102| [What are the steps to use animation module?](#what-are-the-steps-to-use-animation-module)|
|103| [What is State function?](#what-is-state-function)|
|104| [What is Style function?](#what-is-style-function)|
|105| [What is the purpose of animate function?](#what-is-the-purpose-of-animate-function)|
|106| [What is transition function?](#what-is-transition-function)|
|107| [How to inject the dynamic script in angular?](#how-to-inject-the-dynamic-script-in-angular)|
|108| [What is a service worker and its role in Angular?](#what-is-a-service-worker-and-its-role-in-angular)|
|109| [What are the design goals of service workers?](#what-are-the-design-goals-of-service-workers)|
|110| [What are the differences between AngularJS and Angular with respect to dependency injection?](#what-are-the-differences-between-angularjs-and-angular-with-respect-to-dependency-injection)|
|111| [What is Angular Ivy?](#what-is-angular-ivy)|
|112| [What are the features included in ivy preview?](#what-are-the-features-included-in-ivy-preview)|
|113| [Can I use AOT compilation with Ivy?](#can-i-use-aot-compilation-with-ivy)|
|114| [What is Angular Language Service?](#what-is-angular-language-service)|
|115| [How do you install angular language service in the project?](#how-do-you-install-angular-language-service-in-the-project)|
|116| [Is there any editor support for Angular Language Service?](#is-there-any-editor-support-for-angular-language-service)|
|117| [Explain the features provided by Angular Language Service?](#explain-the-features-provided-by-angular-language-service)|
|118| [How do you add web workers in your application?](#how-do-you-add-web-workers-in-your-application)|
|119| [What are the limitations with web workers?](#what-are-the-limitations-with-web-workers)|
|120| [What is Angular CLI Builder?](#what-is-angular-cli-builder)|
|121| [What is a builder?](#what-is-a-builder)|
|122| [How do you invoke a builder?](#how-do-you-invoke-a-builder)|
|123| [How do you create app shell in Angular?](#how-do-you-create-app-shell-in-angular)|
|124| [What are the case types in Angular?](#what-are-the-case-types-in-angular)|
|125| [What are the class decorators in Angular?](#what-are-the-class-decorators-in-angular)|
|126| [What are class field decorators?](#what-are-class-field-decorators)|
|127| [What is declarable in Angular?](#what-is-declarable-in-angular)|
|128| [What are the restrictions on declarable classes?](#what-are-the-restrictions-on-declarable-classes)|
|129| [What is a DI token?](#what-is-a-di-token)|
|130| [What is Angular DSL?](#what-is-angular-dsl)|
|131| [What is an rxjs Subject?](#what-is-an-rxjs-Subject)|
|132| [What is Bazel tool?](#what-is-bazel-tool)|
|133| [What are the advantages of Bazel tool?](#what-are-the-advantages-of-bazel-tool)|
|134| [How do you use Bazel with Angular CLI?](#how-do-you-use-bazel-with-angular-cli)|
|135| [How do you run Bazel directly?](#how-do-you-run-bazel-directly)|
|136| [What is platform in Angular?](#what-is-platform-in-angular)|
|137| [What happens if I import the same module twice?](#what-happens-if-i-import-the-same-module-twice)|
|138| [How do you select an element with in a component template?](#how-do-you-select-an-element-with-in-a-component-template)|
|139| [How do you detect route change in Angular?](#how-do-you-detect-route-change-in-angular)|
|140| [How do you pass headers for HTTP client?](#how-do-you-pass-headers-for-http-client)|
|141| [What is the purpose of differential loading in CLI?](#what-is-the-purpose-of-differential-loading-in-cli)|
|142| [Is Angular supports dynamic imports?](#is-angular-supports-dynamic-imports)|
|143| [What is lazy loading?](#what-is-lazy-loading)|
|144| [What are workspace APIs?](#what-are-workspace-apis)|
|145| [How do you upgrade angular version?](#how-do-you-upgrade-angular-version)|
|146| [What is Angular Material?](#what-is-angular-material)|
|147| [How do you upgrade location service of angularjs?](#how-do-you-upgrade-location-service-of-angularjs)|
|148| [What is NgUpgrade?](#what-is-ngupgrade)|
|149| [How do you test Angular application using CLI?](#how-do-you-test-angular-application-using-cli)|
|150| [How to use polyfills in Angular application?](#how-to-use-polyfills-in-angular-application)|
|151| [What are the ways to trigger change detection in Angular?](#what-are-the-ways-to-trigger-change-detection-in-angular)|
|152| [What are the differences of various versions of Angular?](#what-are-the-differences-of-various-versions-of-angular)|
|153| [What are the security principles in angular?](#what-are-the-security-principles-in-angular)|
|154| [What is the reason to deprecate Web Tracing Framework?](#what-is-the-reason-to-deprecate-web-tracing-framework)|
|155| [What is the reason to deprecate web worker packages?](#what-is-the-reason-to-deprecate-web-worker-packages)|
|156| [How do you find angular CLI version?](#how-do-you-find-angular-cli-version)|
|157| [What is the browser support for Angular?](#what-is-the-browser-support-for-angular)|
|158| [What is schematic](#what-is-schematic)|
|159| [What is rule in Schematics?](#what-is-rule-in-schematics)|
|160| [What is Schematics CLI?](#what-is-schematics-cli)|
|161| [What are the best practices for security in angular?](#what-are-the-best-practices-for-security-in-angular)|
|162| [What is Angular security model for preventing XSS attacks?](#what-is-angular-security-model-for-preventing-xss-attacks)|
|163| [What is the role of template compiler for prevention of XSS attacks?](#what-is-the-role-of-template-compiler-for-prevention-of-xss-attacks)|
|164| [What are the various security contexts in Angular?](#what-are-the-various-security-contexts-in-Angular)|
|165| [What is Sanitization? Is angular supports it?](#what-is-sanitization?Is-angular-supports-it)|
|166| [What is the purpose of innerHTML?](#what-is-the-purpose-of-innerhtml)|
|167| [What is the difference between interpolated content and innerHTML?](#what-is-the-difference-between-interpolated-content-and-innerhtml)|
|168| [How do you prevent automatic sanitization?](#how-do-you-prevent-automatic-sanitization)|
|169| [Is safe to use direct DOM API methods in terms of security?](#is-safe-to-use-direct-dom-api-methods-in-terms-of-security)|
|170| [What is DOM sanitizer?](#what-is-dom-sanitizer)|
|171| [How do you support server side XSS protection in Angular application?](#how-do-you-support-server-side-xss-protection-in-angular-application)
|172| [Is angular prevents http level vulnerabilities?](#is-angular-prevents-http-level-vulnerabilities)|
|173| [What are Http Interceptors?](#what-are-http-interceptors)|
|174| [What are the applications of HTTP interceptors?](#what-are-the-applications-of-http-interceptors)|
|175| [Is multiple interceptors supported in Angular?](#is-multiple-interceptors-supported-in-angular)|
|176| [How can I use interceptor for an entire application?](#how-can-i-use-interceptor-for-an-entire-application)|
|177| [How does Angular simplifies Internationalization?](#how-does-angular-simplifies-internationalization)|
|178| [How do you manually register locale data?](#how-do-you-manually-register-locale-data)|
|179| [What are the four phases of template translation?](#what-are-the-four-phases-of-template-translation)|
|180| [What is the purpose of i18n attribute?](#what-is-the-purpose-of-i18n-attribute)|
|181| [What is the purpose of custom id?](#what-is-the-purpose-of-custom-id)|
|182| [What happens if the custom id is not unique?](#what-happens-if-the-custom-id-is-not-unique)|
|183| [Can I translate text without creating an element?](#can-i-translate-text-without-creating-an-element)|
|184| [How can I translate attribute?](#how-can-i-translate-attribute)|
|185| [List down the pluralization categories?](#list-down-the-pluralization-categories)|
|186| [What is select ICU expression?](#what-is-select-icu-expression)|
|187| [How do you report missing translations?](#how-do-you-report-missing-translations)|
|188| [How do you provide build configuration for multiple locales?](#how-do-you-provide-build-configuration-for-multiple-locales)|
|189| [What is an angular library?](#what-is-an-angular-library)|
|190| [What is AOT compiler?](#what-is-aot-compiler)|
|191| [How do you select an element in component template?](#how-do-you-select-an-element-in-component-template)|
|192| [What is TestBed?](#what-is-testbed)|
|193| [What is protractor?](#what-is-protractor)|
|194| [What is collection?](#what-is-collection)|
|195| [How do you create schematics for libraries?](#how-do-you-create-schematics-for-libraries)|
|196| [How do you use jquery in Angular?](#how-do-you-use-jquery-in-angular)|
|197| [What is the reason for No provider for HTTP exception?](#what-is-the-reason-for-no-provider-for-http-exception)|
|198| [What is router state?](#what-is-router-state)|
|199| [How can I use SASS in angular project?](#how-can-i-use-sass-in-angular-project)|
|200| [What is the purpose of hidden property?](#what-is-the-purpose-of-hidden-property)|
|201| [What is the difference between ngIf and hidden property?](#what-is-the-difference-between-ngif-and-hidden-property)|
|202| [What is slice pipe?](#what-is-slice-pipe)|
|203| [What is index property in ngFor directive?](#what-is-index-property-in-ngfor-directive)|
|204| [What is the purpose of ngFor trackBy?](#what-is-the-purpose-of-ngfor-trackby)|
|205| [What is the purpose of ngSwitch directive?](#what-is-the-purpose-of-ngswitch-directive)|
|206| [Is it possible to do aliasing for inputs and outputs?](#is-it-possible-to-do-aliasing-for-inputs-and-outputs)|
|207| [What is safe navigation operator?](#what-is-safe-navigation-operator)|
|208| [Is any special configuration required for Angular9?](#is-any-special-configuration-required-for-angular9)|
|209| [What are type safe TestBed API changes in Angular9?](#what-are-type-safe-testbed-api-changes-in-angular9)|
|210| [Is mandatory to pass static flag for ViewChild?](#is-mandatory-to-pass-static-flag-for-viewchild)|
|211| [What are the list of template expression operators?](#what-are-the-list-of-template-expression-operators)
|212| [What is the precedence between pipe and ternary operators?](#what-is-the-precedence-between-pipe-and-ternary-operators)
|213| [What is an entry component?](#what-is-an-entry-component)|
|214| [What is a bootstrapped component?](#what-is-a-bootstrapped-component)|
|215| [How do you manually bootstrap an application?](#how-do-you-manually-bootstrap-an-application)|
|216| [Is it necessary for bootstrapped component to be entry component?](#is-it-necessary-for-bootstrapped-component-to-be-entry-component)|
|217| [What is a routed entry component?](#what-is-a-routed-entry-component#)|
|218| [Why is not necessary to use entryComponents array every time?](#why-is-not-necessary-to-use-entrycomponents-array-every-time)|
|219| [Do I still need to use entryComponents array in Angular9?](#do-i-still-need-to-use-entrycomponents-array-in-angular9#)|
|220| [Is it all components generated in production build?](#is-it-all-components-generated-in-production-build)|
|221| [What is Angular compiler?](#what-is-angular-compiler)|
|222| [What is the role of ngModule metadata in compilation process?](#what-is-the-role-of-ngmodule-metadata-in-compilation-process)|
|223| [How does angular finds components, directives and pipes?](#how-does-angular-finds-components-directives-and-pipes)|
|224| [Give few examples for NgModules?](#give-few-examples-for-ngmodules)|
|225| [What are feature modules?](#what-are-feature-modules)|
|226| [What are the imported modules in CLI generated feature modules?](#what-are-the-imported-modules-in-cli-generated-feature-modules)|
|227| [What are the differences between ngmodule and javascript module?](#what-are-the-differences-between-ngmodule-and-javascript-module)|
|228| [What are the possible errors with declarations?](#what-are-the-possible-errors-with-declarations)|
|229| [What are the steps to use declaration elements?](#what-are-the-steps-to-use-declaration-elements)|
|230| [What happens if browserModule used in feature module?](#what-happens-if-browsermodule-used-in-feature-module)|
|231| [What are the types of feature modules?](#what-are-the-types-of-feature-modules)|
|232| [What is a provider?](#what-is-a-provider)|
|233| [What is the recommendation for provider scope?](#what-is-the-recommendation-for-provider-scope#)|
|234| [How do you restrict provider scope to a module?](#how-do-you-restrict-provider-scope-to-a-module)|
|235| [How do you provide a singleton service?](#how-do-you-provide-a-singleton-service)|
|236| [What are the different ways to remove duplicate service registration?](#what-are-the-different-ways-to-remove-duplicate-service-registration)|
|237| [How does forRoot method helpful to avoid duplicate router instances?](#how-does-forroot-method-helpful-to-avoid-duplicate-router-instances)|
|238| [What is a shared module?](#what-is-a-shared-module)|
|239| [Can I share services using modules?](#can-i-share-services-using-modules)|
|240| [How do you get current direction for locales??](#how-do-you-get-current-direction-for-locales)|
|241| [What is ngcc?](#what-is-ngcc)|
|242| [What classes should not be added to declarations?](#what-classes-should-not-be-added-to-declarations)|
|243| [What is ngzone?](#what-is-ngzone)|
|244| [What is NoopZone?](#what-is-noopzone)|
|245| [How do you create displayBlock components?](#how-do-you-create-displayblock-components)|
|246| [What are the possible data change scenarios for change detection?](#what-are-the-possible-data-change-scenarios-for-change-detection)|
|247| [What is a zone context?](#what-is-a-zone-context)|
|248| [What are the lifecycle hooks of a zone?](#what-are-the-lifecycle-hooks-of-a-zone)|
|249| [Which are the methods of NgZone used to control change detection?](#which-are-the-methods-of-ngzone-used-to-control-change-detection)|
|250| [How do you change the settings of zonejs?](#how-do-you-change-the-settings-of-zonejs)|
|251| [How do you trigger an animation?](#how-do-you-trigger-an-animation)|
|252| [How do you configure injectors with providers at different levels?](#how-do-you-configure-injectors-with-providers-at-different-levels)|
|253| [Is it mandatory to use injectable on every service class?](#is-it-mandatory-to-use-injectable-on-every-service-class)|
|254| [What is an optional dependency?](#what-is-an-optional-dependency)|
|255| [What are the types of injector hierarchies?](#what-are-the-types-of-injector-hierarchies)|
|256| [What are reactive forms?](#what-are-reactive-forms)|
|257| [What are dynamic forms?](#what-are-dynamic-forms)|
|258| [What are template driven forms?](#what-are-template-driven-forms)|
|259| [What are the differences between reactive forms and template driven forms?](#what-are-the-differences-between-reactive-forms-and-template-driven-forms)|
|260| [What are the different ways to group form controls?](#what-are-the-different-ways-to-group-form-controls)|
|261| [How do you update specific properties of a form model?](#how-do-you-update-specific-properties-of-a-form-model)|
|262| [What is the purpose of FormBuilder?](#what-is-the-purpose-of-formbuilder)|
|263| [How do you verify the model changes in forms?](#how-do-you-verify-the-model-changes-in-forms)|
|264| [What are the state CSS classes provided by ngModel?](#what-are-the-state-css-classes-provided-by-ngmodel)|
|265| [How do you reset the form?](#how-do-you-reset-the-form)|
|266| [What are the types of validator functions?](#what-are-the-types-of-validator-functions)|
|267| [Can you give an example of built-in validators?](#can-you-give-an-example-of-built-in-validators)|
|268| [How do you optimize the performance of async validators?](#how-do-you-optimize-the-performance-of-async-validators)|
|269| [How to set ngFor and ngIf on the same element?](#how-to-set-ngfor-and-ngif-on-the-same-element)|
|270| [What is host property in css?](#what-is-host-property-in-css)|
|271| [How do you get the current route?](#how-do-you-get-the-current-route)|
|272| [What is Component Test Harnesses?](#what-is-component-test-harnesses)|
|273| [What is the benefit of Automatic Inlining of Fonts?](#what-is-the-benefit-of-automatic-inlining-of-fonts)|
|274| [What is content projection?](#what-is-content-projection)|
|275| [What is ng-content and its purpose?](#what-is-ng-content-and-its-purpose)|
|276| [What is standalone component?](#what-is-standalone-component)|
|277| [How to create a standalone component uing CLI command?](#how-to-create-a-standalone-component-uing-cli-command)
|278| [How to create a standalone component manually?](#how-to-create-a-standalone-component-manually)
|279| [What is hydration ?](#what-is-hydration)
|280| [What are Angular Signals?](#what-are-angular-signals)
|281| [Explain Angular Signals with an example](#explain-angular-signals-with-an-example)
|282| [What are the Route Parameters? Could you explain each of them?](#what-are-the-route-parameters-could-you-explain-each-of-them)
|283| [](#)

1. ### What is Angular Framework?

    Angular is a **TypeScript-based open-source** front-end platform that makes it easy to build web, mobile and desktop applications. The major features of this framework include declarative templates, dependency injection, end to end tooling which ease application development.

  **[⬆ Back to Top](#table-of-contents)**

2. ### What is the difference between AngularJS and Angular?
    Angular is a completely revived component-based framework in which an application is a tree of individual components.

    Here are some of the major differences in tabular format:-

    | AngularJS | Angular |
    |---- | ---------
    | It is based on MVC architecture| This is based on Service/Controller|
    | It uses JavaScript to build the application| Uses TypeScript to build the application|
    | Based on controllers concept| This is a component based UI approach|
    | No support for mobile platforms| Fully supports mobile platforms|
    | Difficult to build SEO friendly application| Ease to build SEO friendly applications|

  **[⬆ Back to Top](#table-of-contents)**

3. ### What is TypeScript?
    **TypeScript** is a programming language that is a superset of JavaScript. It adds features like **static typing** and **classes** to JavaScript, making it easier to catch errors early and write more reliable code. TypeScript code is converted into regular JavaScript before it runs in the browser or on a server.

    In simple terms, TypeScript helps developers write cleaner and more manageable code by providing extra tools and features on top of JavaScript.

    You can install TypeScript globally as
    ```cmd
    npm install -g typescript
    ```
    Let's see a simple example of TypeScript usage:-
    ```typescript
    function greeter(person: string) {
        return "Hello, " + person;
    }

    let user = "Sudheer";

    document.body.innerHTML = greeter(user);
    ```
    The greeter method allows only string type as argument.

  **[⬆ Back to Top](#table-of-contents)**

4. ### Write a pictorial diagram of Angular architecture?
    The main building blocks of an Angular application are shown in the diagram below:-
    ![ScreenShot](images/architecture.png)

  **[⬆ Back to Top](#table-of-contents)**

5. ### What are the key components of Angular?
    Angular has the key components below,

1. **Component**:
   - Components are the fundamental building blocks of an Angular application. They control a view (HTML template) and handle user interactions, rendering data, and managing the application logic.
   - Every Angular application has at least one component, the root component, which serves as the entry point.
   - Components consist of three parts: 
     - **HTML Template** (defines the view)
     - **CSS Styles** (for styling the view)
     - **Class** (for handling the logic, data, and interaction)

2. **Modules**:
   - An Angular module (`@NgModule`) is a container for a group of related components, directives, services, and other Angular features. It helps organize an application into cohesive blocks of functionality.
   - An Angular application typically has a root module (`AppModule`), and additional feature modules can be created for organizing the code.
   - Modules can import other modules, declare components, and provide services.

3. **Templates**:
   - Templates are HTML files that define the structure and layout of the view for a component. They can contain Angular directives (like `*ngIf`, `*ngFor`) and data-binding expressions (like `{{ variable }}`) to dynamically display content based on the component’s data.
   - Templates also handle user interactions through event binding and two-way data binding.

4. **Services**:
   - Services are used to encapsulate business logic and share data and functionality across multiple components. They are classes with specific logic, such as fetching data from an API, handling authentication, or performing other reusable tasks.
   - Angular services are typically injected into components using **dependency injection (DI)**, ensuring they are reusable and maintainable.

5. **Metadata**:
   - Metadata provides additional information about Angular classes, typically used with decorators like `@Component`, `@NgModule`, `@Injectable`, etc.
   - It allows Angular to understand how to process or interact with a class. For instance, `@Component` metadata defines the template, selector, and other properties of a component.

6. **Directives**:
   - Directives are special markers or attributes that extend the functionality of elements in the DOM.
   - There are three types of directives:
     - **Structural Directives**: Change the structure of the DOM, like `*ngIf`, `*ngFor`, and `ngSwitch`.
     - **Attribute Directives**: Change the appearance or behavior of an element, like `ngClass`, `ngStyle`, and `ngModel`.
     - **Custom Directives**: Developers can create custom directives to encapsulate custom behaviors.

7. **Pipes**:
   - Pipes are used to transform data in templates, such as formatting dates, currency, or converting text to uppercase. They can be built-in pipes or custom pipes.
   - Example of built-in pipes: `date`, `currency`, `json`, `uppercase`, etc.

8. **Routing**:
   - The Angular Router is used to navigate between different views or pages in a single-page application (SPA). It maps URLs to components and manages navigation state.
   - Routes are defined in the routing module, and the router displays the corresponding component when a user navigates to a specific URL.

9. **Dependency Injection (DI)**:
   - Dependency Injection is a design pattern that allows components and services to receive their dependencies (such as other services or data) rather than creating them internally. This promotes loose coupling and makes the application easier to test and maintain.

10. **Change Detection**:
    - Angular uses a change detection mechanism to keep the view in sync with the underlying data model. When the model changes, Angular detects the change and updates the view accordingly.
    - It uses a strategy called **zone.js** to detect changes automatically and triggers change detection whenever an event occurs (e.g., user input, HTTP response).

11. **Forms**:
    - Angular provides two types of forms: **Template-driven forms** and **Reactive forms**.
      - **Template-driven forms** rely on Angular's directives in the template (e.g., `ngModel`) for two-way data binding.
      - **Reactive forms** provide more control and flexibility with an explicit model defined in the component. They are more suitable for complex forms and validation scenarios.

12. **HttpClient**:
    - The `HttpClient` module in Angular is used to send HTTP requests and handle responses. It provides methods like `get()`, `post()`, `put()`, and `delete()` to interact with REST APIs and other web services.

13. **Animations**:
    - Angular provides a robust animation framework that helps create smooth animations in the application. The Angular animations API allows developers to define complex animations based on events and triggers, improving the user experience.

14. **Testing**:
    - Angular supports unit testing using **Jasmine**, **Karma**, and **Protractor** for end-to-end testing. Components, services, and other parts of the application can be tested in isolation with mocks and spies to ensure they work correctly.
  
15. **Life Cycle Hooks**:
    - Angular provides lifecycle hooks that allow you to tap into key events during the life of a component or directive (e.g., `ngOnInit`, `ngOnChanges`, `ngOnDestroy`, etc.). These hooks provide a way to perform actions at various points during a component's lifecycle.
16. **Decorators**:
    In Angular, **decorators** are special functions that add metadata to classes, methods, properties, or parameters. These metadata inform Angular how to process those elements, such as how to handle components, services, or directives.

    Some common Angular decorators are:

    1. **@Component**: Marks a class as an Angular component and defines its metadata, such as template and styles.
    2. **@Injectable**: Marks a class as available for dependency injection (DI).
    3. **@Directive**: Marks a class as an Angular directive.
    4. **@NgModule**: Defines an Angular module and its components, directives, and services.


### **Summary of Key Angular Components**:

1. **Component**: Basic building block for views and logic.
2. **Modules**: Group related components, directives, and services.
3. **Templates**: Define the structure and layout of the view.
4. **Services**: Handle reusable business logic and shared functionality.
5. **Metadata**: Used by decorators to provide configuration to Angular classes.
6. **Directives**: Extend HTML elements’ behavior.
7. **Pipes**: Transform data in templates.
8. **Routing**: Manage navigation and URL mapping.
9. **Dependency Injection (DI)**: Manage dependencies for components and services.
10. **Change Detection**: Keep the view updated with model changes.
11. **Forms**: Handle user input via template-driven or reactive forms.
12. **HttpClient**: Handle HTTP requests and responses.
13. **Animations**: Enhance the user interface with animations.
14. **Testing**: Tools and frameworks for testing components and services.
15. **Life Cycle Hooks**: Enable actions at specific points in a component's life cycle.

  **[⬆ Back to Top](#table-of-contents)**

11. ### What are lifecycle hooks available?
    **Lifecycle hooks** in Angular are methods that are called at different stages of a component's lifecycle, from creation to destruction. These hooks allow you to run custom code during specific phases of the component's lifecycle, such as initialization or changes in data.

    ![ScreenShot](images/lifecycle.png)

    The description of each lifecycle method is as below,
   - **`ngOnInit()`**: Called after the component's constructor and after the first `ngOnChanges`. It's used for component initialization, such as fetching data.
   - **`ngOnChanges()`**: Called when an input property of the component changes. It gets called before `ngOnInit()` and whenever an input property is updated.
   - **`ngDoCheck()`**: Called during every change detection cycle. It's a place to perform custom change detection.
   - **`ngAfterViewInit()`**: Called after the component's view and child views have been initialized.
   - **`ngAfterViewChecked()`**: Called after the component's view and child views have been checked.
   - **`ngOnDestroy()`**: Called just before Angular destroys the component. It is useful for cleanup tasks like unsubscribing from observables or removing event listeners.

6. ### What are directives?
    In Angular, **directives** are special markers (attributes or elements) in the DOM that tell Angular to do something to a DOM element, component, or another directive. They are used to add behavior to elements in the HTML template.

    There are three types of directives in Angular:

    1. **Components**: These are technically directives with a template. They define both the logic and view for a part of the UI.
    2. **Structural Directives**: These change the structure of the DOM by adding or removing elements. Examples include:
      - `*ngIf`: Conditionally includes an element in the DOM.
      - `*ngFor`: Loops through data and renders a template for each item.
      
    3. **Attribute Directives**: These change the appearance or behavior of an element, component, or another directive. Examples include:
      - `ngClass`: Adds or removes CSS classes based on some condition.
      - `ngStyle`: Changes the style of an element dynamically.

    #### Example:

    1. **Structural Directive (`*ngIf`)**:

    ```html
    <div *ngIf="isVisible">This content is visible if isVisible is true.</div>
    ```

    2. **Attribute Directive (`ngClass`)**:

    ```html
    <div [ngClass]="{'active': isActive}">This element has an active class based on the condition.</div>
    ```

    #### In Summary:
    **Directives** in Angular are used to modify the behavior or structure of the DOM elements. They can change the appearance, behavior, or layout of the elements, and are used to add reusable functionality to the templates.
  **[⬆ Back to Top](#table-of-contents)**

7. ### What are components?
    A **component** in Angular is a building block of the user interface (UI). It controls a part of the screen (a view) and contains the logic to manage that view. Components are responsible for rendering the UI, handling user input, and interacting with services or other parts of the application.

    #### Key Points:
    1. **Template**: The HTML that defines the view or structure of the UI.
    2. **Class**: The TypeScript code that defines the behavior and logic of the component.
    3. **Metadata**: The `@Component` decorator, which provides configuration for the component, such as the selector, template, and styles.

    #### Example:
    Here’s a simple example of an Angular component:

    ```typescript
    import { Component } from '@angular/core';

    @Component({
      selector: 'app-my-component', // The component's HTML tag
      template: '<h1>{{ message }}</h1>', // The template that renders the view
      styleUrls: ['./my-component.component.css'] // Optional styles for the component
    })
    export class MyComponent {
      message = 'Hello, Angular!'; // Logic to bind data to the template
    }
    ```

    #### In Summary:
    A **component** in Angular is a self-contained unit that defines a part of the user interface and the logic for that part. It includes a template (HTML), a class (TypeScript), and styles, all working together to display and control a section of the app's UI.

  **[⬆ Back to Top](#table-of-contents)**

8. ### What are the differences between Component and Directive?
    In a short note, A component(@component) is a directive-with-a-template.

    Some of the major differences are mentioned in a tabular form

    | Component | Directive |
    |---- | ---------
    | To register a component we use @Component meta-data annotation  | To register a directive we use @Directive meta-data annotation |
    | Components are typically used to create UI widgets| Directives are used to add behavior to an existing DOM element |
    | Component is used to break down the application into smaller components| Directive is used to design re-usable components|
    | Only one component can be present per DOM element | Many directives can be used per DOM element |
    | @View decorator or templateurl/template are mandatory | Directive doesn't use View|

  **[⬆ Back to Top](#table-of-contents)**

9. ### What is a decorators?
   **Decorators** in Angular are special functions used to add metadata to classes, properties, methods, and parameters. They provide a way to define configuration or behavior for various Angular entities such as components, directives, services, pipes, etc.

   - **Role**: Decorators enable Angular to understand how to treat different classes and properties. They allow you to define how Angular should behave with those classes in terms of dependency injection, component lifecycle, and more.
   - **Common Decorators**:
     - **`@Component`**: Marks a class as a component and provides metadata for Angular to render the component's template.
     - **`@Directive`**: Marks a class as a directive, used for manipulating the DOM.
     - **`@Injectable`**: Marks a class as a service that can be injected into other components or services.
     - **`@NgModule`**: Defines an Angular module, which organizes components, services, directives, and other modules.
     - **`@Input`**: Declares a property as an input to a component, allowing data to be passed into the component from its parent.
     - **`@Output`**: Declares a property as an output event, allowing the component to emit events to its parent.
     - **`@HostListener`**: Used to listen to events on the DOM element associated with the directive or component.

   Example of a component decorator:
   ```typescript
   @Component({
     selector: 'app-my-component',
     templateUrl: './my-component.component.html',
     styleUrls: ['./my-component.component.css']
   })
   export class MyComponent {
     // component logic
   }
   ```

   **Decorators** are central to Angular’s configuration system and are used to define the behavior of various entities in Angular applications.

10. ### What is a module?
     **Modules** in Angular are used to organize an application into cohesive blocks of functionality. Every Angular application has at least one module, known as the root module (`AppModule`). Modules can contain:
   - Components
   - Directives
   - Pipes
   - Services
   - Other modules (imported or exported)
   
    Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application.
    Lets take an example of **app.module.ts** root module declared with **@NgModule** decorator as below,
    ```typescript
    import { NgModule }      from '@angular/core';
    import { BrowserModule } from '@angular/platform-browser';
    import { AppComponent }  from './app.component';

    @NgModule ({
       imports:      [ BrowserModule ],
       declarations: [ AppComponent ],
       bootstrap:    [ AppComponent ],
       providers: []
    })
    export class AppModule { }
    ```
    The NgModule decorator has five important (among all) options:
    1. The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application.
    2. The declarations option is used to define components in the respective module.
    3. The bootstrap option tells Angular which Component to bootstrap in the application.
    4. The providers option is used to configure a set of injectable objects that are available in the injector of this module.
    5. The entryComponents option is a set of components dynamically loaded into the view.

  **[⬆ Back to Top](#table-of-contents)**

16. ### What is a service?
    A **service** in Angular is a class that provides reusable logic, like data handling or utility functions, and is typically injected into components or other services using **dependency injection**. Services promote code reusability and help in organizing logic in a modular way.

    Let's create a repoService which can be used across components,

    ```typescript
    import { Injectable } from '@angular/core';
    import { Http } from '@angular/http';

    @Injectable({ // The Injectable decorator is required for dependency injection to work
      // providedIn option registers the service with a specific NgModule
      providedIn: 'root',  // This declares the service with the root app (AppModule)
    })
    export class RepoService{
      constructor(private http: Http){
      }

      fetchAll(){
        return this.http.get('https://api.github.com/repositories');
      }
    }
    ```
    The above service uses Http service as a dependency.

  **[⬆ Back to Top](#table-of-contents)**

17. ### What is dependency injection in Angular?
    **Dependency Injection (DI)** in Angular is a pattern that allows Angular to automatically provide services or other dependencies to components and services. It improves code maintainability, testability, and reusability by managing how dependencies are provided and shared across an application.

232. ### What is a provider?
     A **provider** in Angular is a mechanism that tells Angular how to create a service or value to be injected into components or other services. It is a key part of the **dependency injection** system in Angular, allowing you to manage the creation and sharing of services.

    #### Example of a Service Provider:
    In an Angular application, you define a provider for a service in the `@NgModule` or `@Component` decorator.

    ```typescript
    import { Injectable } from '@angular/core';

    @Injectable({
      providedIn: 'root', // This makes the service globally available
    })
    export class MyService {
      constructor() { }
      
      getServiceData() {
        return 'Some data from the service';
      }
    }
    ```
     ```
     **[⬆ Back to Top](#table-of-contents)**

28. ### What are pipes?
    **Pipes** in Angular are used to transform data before displaying it in the template. They are commonly used to format data, like dates, currency, or custom transformations (e.g., filtering a list). Angular comes with several built-in pipes like `date`, `currency`, `json`, and `uppercase`.

    - **Custom pipes** can be created by implementing the `PipeTransform` interface and using the `@Pipe` decorator. The custom pipe needs to define the `transform` method that will receive the input data and return the transformed result.

    Example of creating a custom pipe:
    ```typescript
    import { Pipe, PipeTransform } from '@angular/core';
    
    @Pipe({
      name: 'exponentialStrength'
    })
    export class ExponentialStrengthPipe implements PipeTransform {
      transform(value: number, exponent: number = 1): number {
        return Math.pow(value, exponent);
      }
    }
    ```
    Usage in the template:
    ```html
    <div>{{ 2 | exponentialStrength:10 }}</div>
    ```

  **[⬆ Back to Top](#table-of-contents)**

34. ### What is a bootstrapping module?
    In Angular, a **bootstrapping module** is the module responsible for initializing and starting up an Angular application. It is the entry point of the application and tells Angular which component to load first when the application starts.

    #### Key Points:
    1. **Root Module**: The bootstrapping module is usually the **root module** (often named `AppModule`).
    2. **Bootstrapping**: During the bootstrapping process, Angular loads the root component (usually `AppComponent`) and sets up the application for rendering.
    3. **`platformBrowserDynamic().bootstrapModule()`**: This is the function Angular uses to start the bootstrapping process in the browser. It bootstraps the root module (`AppModule`) and starts the Angular application.

    #### Example:
    In the `main.ts` file of an Angular application, you’ll typically see something like this:

    ```typescript
    import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';
    import { AppModule } from './app/app.module';

    platformBrowserDynamic().bootstrapModule(AppModule)
      .catch(err => console.error(err));
    ```

    #### In Summary:
    A **bootstrapping module** in Angular is the module that Angular uses to start the application by loading the root component. It initializes the app and begins the rendering process. This is typically the **AppModule** in most Angular applications.

  **[⬆ Back to Top](#table-of-contents)**


40. ### What is RxJS and how is it used in Angular?
    **RxJS** (Reactive Extensions for JavaScript) is a library for reactive programming using **Observables**, which allows you to compose asynchronous and event-based programs using operators like `map`, `filter`, `merge`, and `switchMap`.

   - **Observables** in RxJS are used to handle asynchronous data streams (e.g., HTTP requests, user inputs, etc.).
   - In Angular, RxJS is heavily used for managing asynchronous operations, especially with the **HttpClient** service, where API calls return **Observables**.
   - RxJS is also used for handling events (e.g., user clicks), time-based actions (e.g., intervals, timeouts), and more.

   Example of using RxJS with Angular's HttpClient:
   ```typescript
   import { HttpClient } from '@angular/common/http';
   import { Observable } from 'rxjs';
   import { catchError } from 'rxjs/operators';

   @Injectable({
     providedIn: 'root'
   })
   export class DataService {
     constructor(private http: HttpClient) {}

     getData(): Observable<any> {
       return this.http.get('https://api.example.com/data').pipe(
         catchError(err => {
           console.error('Error occurred:', err);
           throw err;
         })
       );
     }
   }
   ```

   In this example, `getData()` returns an **Observable**, and we use RxJS operators like `pipe` and `catchError` to manage errors and data transformations.

  **[⬆ Back to Top](#table-of-contents)**

41. ### What is subscribing?
    **Subscribing** in Angular (and RxJS) means telling an observable to start sending its data to you. When you **subscribe** to an observable, you listen for the values it emits (such as results from an HTTP request, user actions, or time-based events).

    #### Key Points:
    - **Subscribing** means you are "watching" or "listening" to an observable.
    - You provide a function (or object) that handles the data when it's emitted.
    - Once subscribed, the observable starts emitting values and the subscriber gets those values automatically.

    #### Example:
    ```typescript
    import { Observable } from 'rxjs';

    // Create an observable that emits values
    const myObservable = new Observable(subscriber => {
      subscriber.next('Hello');
      subscriber.next('World');
      subscriber.complete();  // Marks the observable as complete
    });

    // Subscribe to the observable
    myObservable.subscribe({
      next: (value) => console.log(value),  // Handle each emitted value
      complete: () => console.log('Done')  // Handle when the observable completes
    });
    ```

    #### In Simple Terms:
    **Subscribing** is when you "tune in" to an observable to receive its data or updates. Once you subscribe, you get notified whenever the observable emits new data.

  **[⬆ Back to Top](#table-of-contents)**

42. ### What is an observable?
    An **observable** is a way to manage and work with asynchronous data or events in Angular. It represents a stream of data that can emit multiple values over time, like data from an HTTP request, user input, or a timer. You "subscribe" to an observable to receive the emitted values and react to them as they come in.

    In simple terms, an observable is like a TV channel that you can tune into (subscribe) to receive updates (data or events).

   ### Key Points:
  - **Asynchronous**: Observables can handle data that comes in over time, like the result of an HTTP request or events triggered by the user.
  - **Emit Values**: An observable can emit multiple values (e.g., data, events) over time.
  - **Subscribe**: To receive the values emitted by an observable, you **subscribe** to it. Once subscribed, the observer (subscriber) will receive data updates automatically.

    Let see the simple example of observable,
    ### Example of an Observable:
    ```typescript
    import { Observable } from 'rxjs';

    // Create a simple observable
    const myObservable = new Observable(subscriber => {
      subscriber.next('Hello');
      subscriber.next('World');
      subscriber.complete();  // Marks the observable as complete
    });

    // Subscribe to the observable
    myObservable.subscribe({
      next: (value) => console.log(value),
      complete: () => console.log('Done')
    });
    ```

  **[⬆ Back to Top](#table-of-contents)**

43. ### What is an observer?
    Observer is an interface for a consumer of push-based notifications delivered by an Observable. It has below structure,

    ```javascript
    interface Observer<T> {
      closed?: boolean;
      next: (value: T) => void;
      error: (err: any) => void;
      complete: () => void;
    }
    ```
    A handler that implements the Observer interface for receiving observable notifications will be passed as a parameter for observable as below,

    ```javascript
    myObservable.subscribe(myObserver);
    ```
    **Note:** If you don't supply a handler for a notification type, the observer ignores notifications of that type.

  **[⬆ Back to Top](#table-of-contents)**

45. ### What is multicasting?
    **Multicasting** is a way of sharing a single data stream (like an HTTP request or event) with multiple subscribers without triggering the operation multiple times. This makes the process more efficient, as all subscribers receive the same data from a single execution.

    Here's an example that demonstrates multicasting with the `share()` operator.

    ```typescript
    import { Observable } from 'rxjs';
    import { share } from 'rxjs/operators';

    const dataObservable = new Observable(observer => {
      console.log('HTTP request made');
      observer.next('data');
      observer.complete();
    }).pipe(
      share()  // Share the same observable for multiple subscribers
    );

    dataObservable.subscribe(data => {
      console.log('Subscriber 1:', data);
    });

    dataObservable.subscribe(data => {
      console.log('Subscriber 2:', data);
    });
    ```

    In this case, "HTTP request made" will be logged **only once**, even though there are two subscribers, because of the `share()` operator.

    ### Why Use Multicasting:
    - **Efficiency**: Multicasting reduces unnecessary executions of expensive operations, like HTTP requests or complex calculations.
    - **Shared Data**: It allows multiple parts of the application to listen to and act on the same data stream, such as user input or real-time updates.
      
    ### In Summary:
    **Multicasting** in Angular allows multiple subscribers to share the same observable execution, reducing redundant operations and making the application more efficient. You can achieve multicasting using operators like `share()` or `publish()`.



  **[⬆ Back to Top](#table-of-contents)**

63. ### What is Angular Router?
    **Angular Router** is a powerful library in Angular that allows you to navigate between different views or pages within a single-page application (SPA) based on the URL. It provides a way to map URLs to components and manage navigation, including features like lazy loading, route guards, and more.

    #### Key Features:
    1. **Routing to Components**: The router maps specific URLs to components, allowing you to display different views based on the URL.
    2. **Navigation**: You can programmatically navigate between views, either using router links in templates or via the `Router` service.
    3. **Route Parameters**: Angular Router supports passing parameters in the URL (e.g., for dynamic content like user profiles).
    4. **Lazy Loading**: Modules can be loaded only when needed, improving app performance.
    5. **Route Guards**: You can control access to certain routes based on conditions like authentication.

    #### Basic Example:
    1. **Define Routes** in `app-routing.module.ts`:

      ```typescript
      import { NgModule } from '@angular/core';
      import { RouterModule, Routes } from '@angular/router';
      import { HomeComponent } from './home/home.component';
      import { AboutComponent } from './about/about.component';

      const routes: Routes = [
        { path: '', component: HomeComponent },  // Default route
        { path: 'about', component: AboutComponent }
      ];

      @NgModule({
        imports: [RouterModule.forRoot(routes)],
        exports: [RouterModule]
      })
      export class AppRoutingModule {}
      ```

    2. **Linking to Routes** in the HTML template:

      ```html
      <a routerLink="/">Home</a>
      <a routerLink="/about">About</a>
      ```

    3. **Router Outlet**: Where the routed components will be displayed in the HTML template:

      ```html
      <router-outlet></router-outlet>
      ```

    #### In Summary:
    **Angular Router** is used to manage navigation between views or pages in a single-page application. It maps URLs to components and allows for features like dynamic routing, lazy loading, and route guards.

  **[⬆ Back to Top](#table-of-contents)**

98. ### What is zone?
    In Angular, a **zone** is a mechanism used to track asynchronous operations like HTTP requests, timeouts, or promises. It helps Angular know when to update the UI after such tasks are completed. 

    **Zone.js** is the library Angular uses to manage zones, which automatically triggers **change detection** and updates the view when asynchronous tasks finish.



  **[⬆ Back to Top](#table-of-contents)**

 120. ### What is Angular CLI?
    The **Angular CLI** (Command Line Interface) is a powerful tool that helps developers automate tasks during the Angular application development process. It provides commands for creating, testing, building, and deploying Angular projects, significantly improving developer productivity and standardizing workflows.

   Key roles and features of Angular CLI:
   - **Project setup**: It allows you to quickly generate a new Angular project with a pre-configured build setup.
   - **Generate components, services, modules**: You can generate Angular components, services, modules, pipes, directives, and other files with simple CLI commands.
     ```bash
     ng generate component my-component
     ```
   - **Building and bundling**: The CLI compiles and bundles the application for production, including optimization techniques like tree shaking and minification.
     ```bash
     ng build --prod
     ```
   - **Running development server**: The CLI provides a development server to preview the application during development.
     ```bash
     ng serve
     ```
   - **Testing**: The CLI supports unit testing with frameworks like Jasmine and Karma, and end-to-end testing with Protractor.
     ```bash
     ng test
     ```
   - **Deployment**: It provides tools for deploying the application to different environments or hosting platforms.

   The CLI simplifies many tasks and ensures Angular applications follow best practices.

   **[⬆ Back to Top](#table-of-contents)**

52. ### *How to implement authgaurd n angular?
  **Route guards** in Angular are used to control access to different routes based on certain conditions, such as user authentication, role-based access, or unsaved changes in a form. Route guards can be used to prevent navigation to a route or to prompt the user before navigating away from a route.

   There are several types of route guards:
   - **`CanActivate`**: Determines if a route can be activated or not. It is used for protecting routes from unauthorized access.
   - **`CanDeactivate`**: Prevents navigation away from a route if the user has unsaved changes or needs to confirm the navigation.
   - **`CanLoad`**: Prevents the loading of lazy-loaded modules based on certain conditions.
   - **`Resolve`**: Resolves data before activating a route, often used for pre-fetching data before a component is loaded.

   Example of a **`CanActivate` guard**:
   ```typescript
   import { Injectable } from '@angular/core';
   import { CanActivate, ActivatedRouteSnapshot, RouterStateSnapshot, Router } from '@angular/router';
   import { AuthService } from './auth.service';

   @Injectable({
     providedIn: 'root'
   })
   export class AuthGuard implements CanActivate {
     constructor(private authService: AuthService, private router: Router) {}

     canActivate(
       next: ActivatedRouteSnapshot,
       state: RouterStateSnapshot
     ): boolean {
       if (this.authService.isAuthenticated()) {
         return true;
       } else {
         this.router.navigate(['/login']);
         return false;
       }
     }
   }
   ```

   In the routing configuration:
   ```typescript
   const routes: Routes = [
     { path: 'dashboard', component: DashboardComponent, canActivate: [AuthGuard] },
   ];
   ```

173. ### What are Http Interceptors?
    **Http Interceptors** in Angular are a powerful feature used to modify or handle HTTP requests and responses globally before they reach the backend server or the application components. They allow you to add logic for tasks such as adding authentication tokens, logging, modifying requests, handling errors, and caching responses, all in a central place.

    #### Key Features of Http Interceptors:
    - **Intercept HTTP Requests**: You can modify or add headers, such as adding authentication tokens, to outgoing requests.
    - **Intercept HTTP Responses**: You can inspect or transform the server's response before it's passed to the components.
    - **Error Handling**: Interceptors can catch errors globally and provide consistent error handling.
    - **Global Configuration**: Interceptors are set up globally, making it easier to apply changes across all HTTP calls without needing to modify each individual request.

    #### How Http Interceptors Work:
    - An **Interceptor** is a class that implements the `HttpInterceptor` interface.
    - The interceptor has a method called `intercept()`, which is called for every HTTP request made.
    - You can modify the request or response inside this method before passing them forward to the next handler in the chain.

    #### Example of an Http Interceptor:

    1. **Create an Interceptor**:

      ```typescript
      import { Injectable } from '@angular/core';
      import { HttpInterceptor, HttpRequest, HttpHandler, HttpEvent } from '@angular/common/http';
      import { Observable } from 'rxjs';

      @Injectable()
      export class AuthInterceptor implements HttpInterceptor {

        intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
          // Clone the request to add an authorization token
          const clonedRequest = req.clone({
            headers: req.headers.set('Authorization', 'Bearer your-auth-token')
          });

          // Pass the cloned request to the next handler
          return next.handle(clonedRequest);
        }
      }
      ```

    2. **Register the Interceptor**:

      You need to register the interceptor in the app module's providers array:

      ```typescript
      import { NgModule } from '@angular/core';
      import { BrowserModule } from '@angular/platform-browser';
      import { HTTP_INTERCEPTORS } from '@angular/common/http';
      import { AppComponent } from './app.component';
      import { AuthInterceptor } from './auth.interceptor';

      @NgModule({
        declarations: [AppComponent],
        imports: [BrowserModule],
        providers: [
          { provide: HTTP_INTERCEPTORS, useClass: AuthInterceptor, multi: true }
        ],
        bootstrap: [AppComponent]
      })
      export class AppModule {}
      ```

    #### Use Cases for Http Interceptors:
    1. **Authentication**: Attach an authentication token to every HTTP request automatically.
    2. **Logging**: Log request and response details for debugging or monitoring.
    3. **Error Handling**: Catch errors from HTTP requests globally and show user-friendly messages.
    4. **Caching**: Cache HTTP responses to reduce server load or enhance performance.
    5. **Custom Headers**: Add custom headers to requests for specific functionality.


     **[⬆ Back to Top](#table-of-contents)**

143. ### What is lazy loading?
     **Lazy loading** is a design pattern in Angular (and other frameworks) that allows you to load parts of an application **only when they are needed**, rather than loading the entire application at once. This helps improve the initial loading time and performance by deferring the loading of certain modules or components until they are actually required by the user.

  #### How Lazy Loading Works in Angular:
    **Lazy loading** is a design pattern in Angular (and other frameworks) that allows you to load parts of an application **only when they are needed**, rather than loading the entire application at once. This helps improve the initial loading time and performance by deferring the loading of certain modules or components until they are actually required by the user.

     ```javascript
     const routes: Routes = [
       {
         path: 'customers',
         loadChildren: () => import('./customers/customers.module').then(module => module.CustomersModule)
       },
       {
         path: 'orders',
         loadChildren: () => import('./orders/orders.module').then(module => module.OrdersModule)
       },
       {
         path: '',
         redirectTo: '',
         pathMatch: 'full'
       }
     ];
     ```

     ### Benefits of Lazy Loading:
	1. **Improved Performance**: By loading only the necessary parts of the application, the initial loading time is reduced.
	2. **Reduced Memory Usage**: Unused modules are not loaded into memory, saving resources.
	3. **Scalability**: Lazy loading helps scale large applications by breaking them into smaller, manageable chunks.

     **[⬆ Back to Top](#table-of-contents)**

192. ### What is TestBed in angular usnit testing?
     **TestBed** in Angular is a testing utility that helps set up the environment for unit tests. It allows you to configure and create Angular components, services, and other dependencies for testing.

    #### Key Points:
    - **TestBed** is used to **configure** modules, **declare components**, and **inject services** for unit tests.
    - It provides a way to set up the **test environment** before running the tests, making it easy to test components and services in isolation.

    #### Example:

    ```typescript
    import { TestBed } from '@angular/core/testing';
    import { MyComponent } from './my.component';

    describe('MyComponent', () => {
    beforeEach(() => {
        TestBed.configureTestingModule({
        declarations: [MyComponent]
        }).compileComponents();
    });

    it('should create the component', () => {
        const fixture = TestBed.createComponent(MyComponent);
        const component = fixture.componentInstance;
        expect(component).toBeTruthy();
    });
    });
    ```

    In simple terms, **TestBed** is the setup tool for Angular unit tests, allowing you to configure and test your Angular components and services.

     **[⬆ Back to Top](#table-of-contents)**

193. ### What is protractor in angular usnit testing?
     **Protractor** is not used for **unit testing** in Angular. It is an **end-to-end (E2E) testing** framework, designed to test the entire application by simulating user interactions in a real browser. 

    For **unit testing** in Angular, tools like **Jasmine** and **Karma** are used to test individual components or services in isolation. 

    In short, **Protractor** is for testing the full application flow (E2E), while **Jasmine** and **Karma** are used for testing smaller units of code (unit testing).
     ```javascript
     npm install -g protractor
     ```

     **[⬆ Back to Top](#table-of-contents)**

194. ### What is collection in angular usnit testing?
     In the context of **unit testing** in Angular, a **collection** typically refers to a group of data, such as an **array** or **list**, that is used in tests to simulate or check how components, services, or pipes handle multiple items.

    #### Example:
    You might test a component that displays a list of users, where the users are stored in an array (a collection). The unit test would check if the component correctly renders each user.

    #### Simple Example:

    ```typescript
    describe('UserListComponent', () => {
    let component: UserListComponent;
    
    beforeEach(() => {
        component = new UserListComponent();
        component.users = ['Alice', 'Bob', 'Charlie'];  // This is a collection (array)
    });

    it('should display the list of users', () => {
        expect(component.users.length).toBe(3);  // Testing the collection's size
    });
    });
    ```

    In simple terms, a **collection** in Angular unit testing refers to a group of data (like an array) used to test how the application handles and interacts with multiple items.

     **[⬆ Back to Top](#table-of-contents)**

44. ### What is the difference between promise and observable?
    Below are the list of differences between promise and observable:

       | Observable | Promise |
       |---- | --------- |
       | Declarative: Computation does not start until subscription, so they can run whenever you need the result | Executes immediately on creation|
       | Provides multiple values over time | Provides only one |
       | Subscribe method is used for error handling that facilitates centralized and predictable error handling | Push errors to the child promises |
       | Provides chaining and subscription to handle complex applications | Uses only `.then()` clause |

  **[⬆ Back to Top](#table-of-contents)**

45. ### How is polyfills in Angular application?
    **Polyfills** in an Angular application are scripts that provide support for newer web features in older browsers. They are used to ensure that your Angular application runs smoothly across a wide range of browsers, even those that do not natively support newer JavaScript features or web APIs.

    #### Purpose of Polyfills:
    - **Compatibility**: Some modern web features, such as newer JavaScript syntax, APIs, or CSS, may not be supported in older browsers like Internet Explorer. Polyfills add support for these features in such browsers.
    - **Ensure Cross-Browser Functionality**: Polyfills allow Angular applications to work consistently across different browsers, including older versions.

    #### How Polyfills Work in Angular:
    1. **Polyfills File**: Angular has a default `polyfills.ts` file that includes necessary polyfills. This file is automatically set up when you create a new Angular project.
    2. **Browser-Specific Polyfills**: In the `polyfills.ts` file, you can enable or disable specific polyfills based on the target browsers. For example, if you want to support Internet Explorer, you can enable relevant polyfills for that browser.
    3. **Conditional Loading**: Polyfills are conditionally loaded depending on the browser's features, ensuring that only the necessary polyfills are included, which can help optimize performance.

    #### Example of Polyfills in `polyfills.ts`:

    ```typescript
    // Required for older browsers like Internet Explorer
    import 'core-js/es/reflect';  // Reflect API for Angular's dependency injection
    import 'zone.js';  // Zone.js for change detection in Angular

    // Polyfill for specific features like promise or fetch, if needed
    // import 'whatwg-fetch'; // Polyfill for fetch API
    ```

    #### Key Polyfills in Angular:
    - **`zone.js`**: Zone.js is a required polyfill that Angular uses to manage asynchronous operations and trigger change detection.
    - **`core-js`**: Provides support for modern JavaScript features like `Promise`, `Object.assign`, `Array.from`, etc.
    - **Other specific polyfills**: Depending on your target browsers, you may need additional polyfills for features like `fetch`, `custom elements`, or `IntersectionObserver`.
    

    **[⬆ Back to Top](#table-of-contents)**


238. ### What is a shared module?
     A **shared module** in Angular is a module that contains common components, directives, pipes, and services that are used across multiple other modules in the application. It helps avoid code duplication by grouping reusable code in one place, which can then be imported into other modules that need it.

    In short, a shared module is used to organize and share commonly used functionality throughout the app.

     For example, the below shared module imports CommonModule, FormsModule for common directives and components, pipes and directives based on the need,
     ```js
     import { CommonModule } from '@angular/common';
     import { NgModule } from '@angular/core';
     import { FormsModule } from '@angular/forms';
     import { UserComponent } from './user.component';
     import { NewUserDirective } from './new-user.directive';
     import { OrdersPipe } from './orders.pipe';

     @NgModule({
      imports:      [ CommonModule ],
      declarations: [ UserComponent, NewUserDirective, OrdersPipe ],
      exports:      [ UserComponent, NewUserDirective, OrdersPipe,
                      CommonModule, FormsModule ]
     })
     export class SharedModule { }
     ```
     ### Benefits:
    - **Avoids duplication**: Common functionality is defined once and reused throughout the app.
    - **Simplifies maintenance**: Changes in shared components, pipes, or directives only need to be made in the shared module.

     **[⬆ Back to Top](#table-of-contents)**

243. ### What is NgZone?
     **`NgZone`** is an Angular service that helps manage **change detection** by keeping track of asynchronous operations, like HTTP requests or timeouts. It ensures that when these operations are completed, Angular knows to update the view.

    ### Example:
    ```typescript
    import { NgZone } from '@angular/core';

    constructor(private ngZone: NgZone) {}

    someMethod() {
    // Running outside Angular's zone (no change detection triggered)
    this.ngZone.runOutsideAngular(() => {
        setTimeout(() => {
        console.log('This is outside Angular zone.');
        }, 1000);
    });

    // Running inside Angular's zone (change detection triggered)
    this.ngZone.run(() => {
        setTimeout(() => {
        console.log('This is inside Angular zone.');
        }, 1000);
    });
    }
    ```

    - **Inside Angular Zone**: Operations trigger Angular's change detection.
    - **Outside Angular Zone**: Operations do not trigger change detection, improving performance for tasks that don't need view updates.

    In short, `NgZone` helps Angular efficiently handle updates and performance by controlling when change detection should run.

     **[⬆ Back to Top](#table-of-contents)**

256. ### What are reactive forms?
     Reactive forms is a model-driven approach for creating forms in a reactive style(form inputs changes over time). These are built around observable streams, where form inputs and values are provided as streams of input values. Let's follow the below steps to create reactive forms,
     1. Register the reactive forms module which declares reactive-form directives in your app
         ```js
         import { ReactiveFormsModule } from '@angular/forms';

         @NgModule({
           imports: [
             // other imports ...
             ReactiveFormsModule
           ],
         })
         export class AppModule { }
         ```
     2. Create a new FormControl instance and save it in the component.
         ```js
         import { Component } from '@angular/core';
         import { FormControl } from '@angular/forms';

         @Component({
           selector: 'user-profile',
           styleUrls: ['./user-profile.component.css']
         })
         export class UserProfileComponent {
           userName = new FormControl('');
         }
         ```
     3. Register the FormControl in the template.
         ```js
         <label>
           User name:
           <input type="text" [formControl]="userName">
         </label>
         ```
     Finally, the component with reactive form control appears as below,
     ```js
     import { Component } from '@angular/core';
     import { FormControl } from '@angular/forms';
	
     @Component({
       selector: 'user-profile',
       styleUrls: ['./user-profile.component.css'],
       template: `
         <label>
           User name:
           <input type="text" [formControl]="userName">
         </label>
       `
     })
     export class UserProfileComponent {
       userName = new FormControl('');
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

258. ### What are template driven forms?
     Template driven forms are model-driven forms where you write the logic, validations, controls etc, in the template part of the code using directives. They are suitable for simple scenarios and uses two-way binding with [(ngModel)] syntax.
     For example, you can create register form easily by following the below simple steps,

     1. Import the FormsModule into the Application module's imports array
         ```js
            import { BrowserModule } from '@angular/platform-browser';
            import { NgModule } from '@angular/core';
            import {FormsModule} from '@angular/forms'
            import { RegisterComponent } from './app.component';
            @NgModule({
              declarations: [
                RegisterComponent,
              ],
              imports: [
                BrowserModule,
                FormsModule
              ],
              providers: [],
              bootstrap: [RegisterComponent]
            })
            export class AppModule { }
         ```
     2. Bind the form from template to the component using ngModel syntax
         ```html
         <input type="text" class="form-control" id="name"
           required
           [(ngModel)]="model.name" name="name">
         ```
     3.  Attach NgForm directive to the <form> tag in order to create FormControl instances and register them
         ```js
         <form #registerForm="ngForm">
         ```
     4. Apply the validation message for form controls
         ```html
         <label for="name">Name</label>
         <input type="text" class="form-control" id="name"
                required
                [(ngModel)]="model.name" name="name"
                #name="ngModel">
         <div [hidden]="name.valid || name.pristine"
              class="alert alert-danger">
           Please enter your name
         </div>
         ```
     5. Let's submit the form with ngSubmit directive and add type="submit" button at the bottom of the form to trigger form submit.
         ```html
         <form (ngSubmit)="onSubmit()" #heroForm="ngForm">
         // Form goes here
         <button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
         ```
     Finally, the completed template-driven registration form will be appeared as follow.
     ```html
     <div class="container">
       <h1>Registration Form</h1>
       <form (ngSubmit)="onSubmit()" #registerForm="ngForm">
         <div class="form-group">
           <label for="name">Name</label>
             <input type="text" class="form-control" id="name"
                    required
                    [(ngModel)]="model.name" name="name"
                    #name="ngModel">
             <div [hidden]="name.valid || name.pristine"
                  class="alert alert-danger">
               Please enter your name
             </div>
         </div>
         <button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
         </form>
     </div>
     ```

     **[⬆ Back to Top](#table-of-contents)**

275. ### What is ng-content and its purpose?
     The ng-content is used to insert the content dynamically inside the component that helps to increase component reusability. 

    ### Purpose:
    - **Content Projection**: It enables you to insert dynamic content from the parent into the child component.
    - **Reusability**: Helps create reusable components where the content can change based on what the parent provides.

    ### Example:
    In a child component template:
    ```html
    <ng-content></ng-content>
    ```

    The parent component can provide content inside the child component:
    ```html
    <app-child>
    <p>This is content from the parent.</p>
    </app-child>
    ```

      **[⬆ Back to Top](#table-of-contents)**

276. ### What is standalone component?
      A **standalone component** in Angular is a component that doesn't require an Angular module (`@NgModule`). It can be used directly on its own, simplifying the structure of your application. You just need to set `standalone: true` in the `@Component` decorator to make it standalone.

    ### Example of a Standalone Component:
    ```typescript
    import { Component } from '@angular/core';

    @Component({
    selector: 'app-standalone',
    template: `<h1>Hello, Standalone Component!</h1>`,
    standalone: true
    })
    export class StandaloneComponent {}
    ```

    ### Key points:
    - **No module needed**: It works independently without being declared in an `@NgModule`.
    - **Self-contained**: The component is self-sufficient, making it easier to use and share.

    This feature was introduced to make Angular apps simpler and reduce boilerplate code, especially in small apps or libraries.

      **[⬆ Back to Top](#table-of-contents)**

280. ### What are Angular Signals?
      **Angular Signals** are a new way to manage reactive state in Angular applications. They allow you to create a piece of state (called a signal) that can be read and updated easily. When the signal's value changes, any part of the application that depends on it automatically updates, making the application more efficient and easier to manage.

    ### Example of Angular Signals:
    ```typescript
        import { signal } from '@angular/core';

        export class ExampleComponent {
        // Create a signal with an initial value
        count = signal(0);

        // Update the signal value
        increment() {
            this.count.set(this.count() + 1);
        }
        }
    ```
    ### Key points:
    - **Signal** holds a value and allows reactive updates.
    - **Efficiency**: Only parts of the app that depend on the signal will update, reducing unnecessary re-renders.
    - **Simplicity**: Simplifies state management compared to using observables.

    In short, Angular Signals provide a lightweight, efficient way to handle state and reactivity in Angular applications.

      **[⬆ Back to Top](#table-of-contents)**

  ### 25. **What is change detection in Angular? How does it work?**
   **Change detection** in Angular refers to the process of checking and updating the view whenever the application's state (the model) changes. Angular uses a mechanism to detect changes in component properties and update the view automatically.

   Angular employs a **change detection strategy**, which can be either:
   - **Default**: Angular checks all components in the component tree for changes on each event (such as user input, HTTP response, etc.).
   - **OnPush**: Angular only checks a component for changes if one of its input properties has changed or an event has occurred within it. This strategy can improve performance by reducing the number of checks Angular performs.

   The change detection process is triggered by events like user interactions, HTTP requests, or timers. When a change is detected, Angular updates the view to reflect the new state.

   ### 28. **How does Angular handle cross-site request forgery (CSRF)?**
   **Cross-Site Request Forgery (CSRF)** is a type of security vulnerability where an attacker tricks a user into making an unwanted request to a different site using the user's credentials. Angular provides several mechanisms to prevent CSRF attacks, but it doesn't handle CSRF out-of-the-box directly. Instead, Angular works in conjunction with server-side protection to mitigate these risks.

   - **Server-Side Protection**: 
     To prevent CSRF, most servers generate a **CSRF token** that must be included with every request that alters data (e.g., POST, PUT, DELETE). This token is typically set as a cookie or in the response header.
     
   - **Angular's Role**:
     Angular provides the ability to send the CSRF token in request headers. You can add the CSRF token to HTTP requests using **HttpClient** interceptors.
   
   Example of adding the CSRF token:
   ```typescript
   import { Injectable } from '@angular/core';
   import { HttpClient, HttpHeaders } from '@angular/common/http';
   
   @Injectable()
   export class MyHttpInterceptor {
     intercept(req, next) {
       const token = localStorage.getItem('csrf_token');
       const cloned = req.clone({
         headers: req.headers.set('X-CSRF-TOKEN', token)
       });
       return next.handle(cloned);
     }
   }
   ```

  ### 49. **How do you configure Angular to work with environment-specific settings (e.g., production vs development)?**
   Angular allows you to configure environment-specific settings using **environment files**. These files contain settings that change depending on the build environment, such as API URLs, logging levels, feature flags, etc.

   - **Environment files**: Angular provides environment configuration files located in the `src/environments/` directory:
     - `environment.ts` for development.
     - `environment.prod.ts` for production.

   These files export an object with environment-specific configurations, like this:
   ```typescript
   // environment.ts (development)
   export const environment = {
     production: false,
     apiUrl: 'https://dev.api.example.com',
   };

   // environment.prod.ts (production)
   export const environment = {
     production: true,
     apiUrl: 'https://api.example.com',
   };
   ```

   - **Configuration in `angular.json`**: In the `angular.json` file, Angular specifies which environment file to use for each build configuration:
   ```json
   "configurations": {
     "production": {
       "fileReplacements": [
         {
           "replace": "src/environments/environment.ts",
           "with": "src/environments/environment.prod.ts"
         }
       ]
     }
   }
   ```

   - **Accessing environment variables**: In components, services, or any part of the app, you can access the environment settings:
   ```typescript
   import { environment } from '../environments/environment';

   console.log(environment.apiUrl); // Logs the appropriate API URL based on the environment
   ```

   **Advantages**:
   - Seamless environment-specific configuration.
   - Build optimization for different environments (production, development).


   ### 51. **What is the purpose of `ChangeDetectionStrategy.OnPush`? How does it optimize performance?**

Angular uses **change detection** to track and respond to changes in data. By default, Angular uses the `ChangeDetectionStrategy.Default`, where it checks the entire component tree for changes whenever an event occurs (like user interaction, HTTP requests, or timers). This can be inefficient, especially for large apps.

**`ChangeDetectionStrategy.OnPush`**: When this strategy is used, Angular only checks a component when:

* Its inputs (bindings) change.
* An event is triggered within the component.
* It manually triggers change detection (e.g., using `ChangeDetectorRef`).

**Performance Optimization**:

* Reduces the number of checks Angular performs by limiting change detection to specific cases.
* Can dramatically improve performance in large applications with complex component trees, reducing unnecessary re-renders.

**Usage Example:**

```typescript
@Component({
  selector: 'app-my-component',
  changeDetection: ChangeDetectionStrategy.OnPush,
  templateUrl: './my-component.component.html'
})
export class MyComponent {
  @Input() data: any;
}
```

### 51. **Can you explain the use of ngContent and ngTemplate in Angular?**
### 1. **`ngContent`**:
- **Purpose**: Used for **content projection**.
- **Use**: Allows you to pass content from a parent component into a child component.
- **Example**: A parent component can place HTML inside a child component, and that content will be rendered inside the child where `ngContent` is defined.

```html
<!-- Parent Component -->
<app-card>
  <h1>Title</h1>
  <p>Description</p>
</app-card>

<!-- Child Component -->
<div class="card">
  <ng-content></ng-content> <!-- Content from parent will be inserted here -->
</div>
```

### 2. **`ngTemplate`**:
- **Purpose**: Defines a reusable **template** that is not immediately rendered.
- **Use**: You can render the content inside `ng-template` later, usually conditionally or dynamically.
  
```html
<ng-template #myTemplate>
  <p>This is inside the template!</p>
</ng-template>
```

- It is often used with directives like `ngIf` or `ngFor` to control when the content should be shown.

In summary:
- `ngContent` is for projecting parent content into a child component.
- `ngTemplate` is for defining a template that can be rendered later.

### 54. **How would you troubleshoot performance issues in Angular? What tools and techniques would you use?**

To troubleshoot performance issues in an Angular application, the following steps and tools are commonly used:

* **Angular DevTools:** Angular DevTools is an official browser extension that allows you to inspect Angular applications. It provides a timeline view for change detection cycles, component tree, and performance profiling.

* **Chrome DevTools (Performance Tab):** Use the Performance tab in Chrome DevTools to capture and analyze the application's runtime performance. Look for excessive JavaScript execution, long tasks, or frequent reflows.

* **Change Detection Profiling:** Identify which components are being checked too frequently by inspecting the change detection cycle with the Angular DevTools or using `ng.probe` in the browser console. This can highlight performance bottlenecks due to excessive or unnecessary checks.

* **Memory Leaks:** Memory leaks can degrade performance over time. Use Chrome DevTools (Memory tab) to check for memory leaks. Tools like `ngOnDestroy` lifecycle hook can help in cleaning up subscriptions, event listeners, and resources.

* **Network Analysis:** Investigate API requests and responses with the Network tab in Chrome DevTools. Look for slow or redundant requests, and optimize them if necessary (e.g., debouncing or caching).

* **Using Lazy Loading and Code Splitting:** Monitor the network requests during the initial load and ensure that only essential parts of the app are loaded initially. Use tools like `webpack-bundle-analyzer` to analyze and reduce the size of the JavaScript bundles.
---


### 55. **How do you handle error handling in RxJS streams?**

In RxJS, error handling can be done using the following strategies:

* **`catchError`**: This operator catches errors in the observable stream and allows you to recover from the error or return an alternative observable (e.g., an empty observable, a default value, etc.).
* **`retry`**: Retries an operation a given number of times if it fails, useful for transient errors.
* **`finalize`**: Executes cleanup code or logic when an observable completes or errors out.

#### Example: Using `catchError` for error handling

```typescript
import  { Observable, of } from 'rxjs';
import { catchError } from 'rxjs/operators';

this.dataService.getData().pipe(
  catchError(error => {
    console.error('Error occurred:', error);
    return of([]); // Return an empty array as fallback data
  })
).subscribe(data => {
  console.log(data);
});
```

In this example, if an error occurs during the HTTP request, it is caught by `catchError`, and a fallback empty array is returned.

---

### 56. **What is the difference between `switchMap`, `concatMap`, and `mergeMap` in RxJS? Provide examples of when to use each.**

These operators are used to manage the inner observables in higher-order mapping operations. They transform the values emitted by an observable into another observable. The difference lies in how they handle concurrency and the order of emissions.

* **`switchMap`**: If a new value is emitted by the source observable, `switchMap` cancels the previous inner observable and switches to the new one. This is useful when only the result of the latest request is needed (e.g., in search or auto-complete scenarios).

  **Use case**: Fetching the latest search results.

  ```typescript
  codesearchTerm$ = new Subject<string>();

  this.searchTerm$.pipe(
    switchMap(term => this.searchService.search(term))
  ).subscribe(results => {
    console.log(results);
  });
  ```

* **`concatMap`**: This operator ensures that the inner observables are executed one after the other (sequentially). Each inner observable will only start after the previous one completes. This is useful when the order of operations matters (e.g., sequential HTTP requests).

  **Use case**: Uploading files one after the other.

  ```typescript
  codefileQueue$.pipe(
    concatMap(file => this.uploadFile(file))
  ).subscribe(response => {
    console.log('File uploaded:', response);
  });
  ```

* **`mergeMap`**: This operator allows the inner observables to run concurrently, and it merges their results as they complete. It is used when you don't need the operations to be sequential but want them to run in parallel.

  **Use case**: Fetching multiple resources concurrently (e.g., loading user data, comments, and posts in parallel).

  ```typescript
  codeuser$.pipe(
    mergeMap(user => this.loadUserPosts(user.id))
  ).subscribe(posts => {
    console.log(posts);
  });
  ```

Here are some advanced Angular interview questions that may be asked by companies like TalentRank, which assess a deeper understanding of Angular concepts and the ability to implement complex features in real-world applications:

### 57. **Explain the difference between `ngOnInit()` and `constructor()` in Angular. When would you use each one?**

   - **Answer**: `ngOnInit()` is a lifecycle hook that is called after Angular has initialized all data-bound properties of a component. It is typically used for logic that requires data binding or initialization of data that may come from services. The `constructor()` is a standard TypeScript feature used to initialize a class instance, but Angular recommends placing component initialization logic (such as fetching data or subscriptions) inside `ngOnInit()` instead of the `constructor()`.

### 58. **What is the difference between `ngFor` and `ngForOf`?**

   - **Answer**: `ngFor` is an alias for `ngForOf` directive. `ngForOf` is a lower-level implementation of the directive that works with iterable objects, like arrays. While they are functionally equivalent, `ngFor` is the preferred shorthand for most applications.

### 59. **How does Angular change detection work? What are the different strategies available?**

   - **Answer**: Angular uses a change detection mechanism to update the view whenever the model changes. The two primary change detection strategies are:
     - **Default**: Checks every component in the tree for changes.
     - **OnPush**: Only checks components when one of its input properties has changed, or an event has occurred within the component, or manually triggered change detection is invoked.

   You can optimize performance by using `OnPush`, as Angular will check only the components that need to be checked.

   ### 63. **What is a `Subject` and `BehaviorSubject` in Angular RxJS? How are they different?**

   - **Answer**: 
     - A **`Subject`** is a special type of `Observable` that allows values to be multicast to many Observers. It doesn't store the last emitted value.
     - A **`BehaviorSubject`** is a type of `Subject` that requires an initial value and always returns the current value to new subscribers. Unlike a `Subject`, it maintains the last value emitted, making it useful for state management or components that need to know the current state on subscription.

  ### 73. **How would you optimize performance in an Angular application?**

   - **Answer**: Some techniques to optimize Angular application performance include:
     - **Lazy Loading**: Load modules only when needed.
     - **Ahead-of-Time (AOT) Compilation**: Pre-compiling the application during build time instead of runtime.
     - **Change Detection Strategy**: Use `OnPush` change detection strategy to reduce unnecessary checks.
     - **Track By Function**: Use `trackBy` in `ngFor` to optimize DOM rendering.
     - **Avoid Complex Computations in Templates**: Perform complex operations in the component rather than in the template to avoid recalculating on every change detection cycle.
     - **Tree Shaking**: Remove unused code during build time.

  ### **1\. Organizing a Large Angular Application**

When organizing a large Angular application, the goal is to keep the codebase modular, scalable, and maintainable. A good folder structure is crucial to achieving this. Here is a sample folder structure:

```lua
codesrc/
|-- app/
|   |-- core/                # Core modules and services, singletons, etc.
|   |   |-- services/        # Shared services (e.g., API, authentication)
|   |   |-- guards/          # Route guards
|   |   |-- interceptors/    # HTTP interceptors
|   |   |-- models/          # Application-wide models
|   |   |-- constants/       # Constants, configuration files
|   |-- shared/              # Shared components, directives, and pipes
|   |   |-- components/      # Reusable components
|   |   |-- directives/      # Reusable directives
|   |   |-- pipes/           # Reusable pipes
|   |-- features/            # Feature modules
|   |   |-- feature1/        # Module for a specific feature (e.g., user management)
|   |   |-- feature2/        # Module for another feature
|   |-- app-routing.module.ts # Centralized routing configuration
|   |-- app.component.ts      # Root component
|   |-- app.module.ts         # Root module (imports Core, Shared, and Feature modules)
|-- assets/                  # Static files (images, fonts, etc.)
|-- environments/            # Environment-specific configurations (prod, dev)
```

#### Key Principles:

* **Modularity**: Split the application into feature modules (`features/`), core services (`core/`), and reusable UI components (`shared/`).
* **Lazy Loading**: Use lazy loading to load feature modules only when required to reduce the initial bundle size.
* **Separation of Concerns**: Each module should have a clear responsibility. For example, authentication logic goes into the `core` module, while UI components like buttons or form controls belong in `shared/`.
* **Services & Dependency Injection**: Angular’s Dependency Injection system helps in managing dependencies between services and components.

#### Managing Dependencies:

* Use **Angular CLI** to manage dependencies and update the application.
* Manage third-party libraries in `package.json`, and prefer modular libraries that can be lazy-loaded to minimize the initial load time.
* Use **barrels** (index.ts files) to re-export modules or components for easier and cleaner imports.

---

### **2\. State Management in Angular**

State management refers to the practice of managing data within an application in a consistent way. It ensures that the application's state (data) is predictable, centralized, and easy to manage, especially in large-scale applications where many components need access to the same data.

#### Tools for State Management in Angular:

* **NgRx**: A popular state management library based on Redux. It helps manage state in a reactive way using actions, reducers, and selectors. NgRx is great for large applications with complex state and side effects. It is well-integrated with Angular's reactive programming model (RxJS).

  * **When to use NgRx**:
    * When the application has complex, global state.
    * When multiple components or modules need to share the same state.
    * When dealing with a lot of asynchronous operations like HTTP requests.
  * **Features of NgRx**:
    * Actions and Reducers for state changes.
    * Effects for handling side effects (like API calls).
    * Selectors for deriving data from the store.
    * DevTools support for time-travel debugging.

* **Akita**: Another state management library for Angular that is simpler than NgRx and offers more flexibility. It is built around the concept of stores, and it’s less boilerplate-heavy compared to NgRx.

  * **When to use Akita**:
    * When you need simpler state management without the full complexity of NgRx.
    * When the application doesn't require advanced features like effects or strict immutability.
  * **Features of Akita**:
    * Simple store-based architecture.
    * Supports both local and remote data storage.
    * Provides built-in tools for managing the lifecycle of entities.

* **Services + BehaviorSubjects**: In smaller apps or isolated parts of an application, you may choose to manage state locally using services and `BehaviorSubject` or `ReplaySubject` to share state between components. This is more lightweight than NgRx or Akita but can get cumbersome in larger apps.

---

### **3\. Designing a Scalable, Maintainable, and Testable Angular Application**

A scalable, maintainable, and testable Angular application can be achieved by adhering to good design principles and best practices:

#### 1\. **Modularity**:

* Break down your application into **feature modules** that encapsulate related functionality. Use **lazy loading** to load modules only when needed.
* Have a clear distinction between **core** services (authentication, routing, etc.), **shared** components (form controls, buttons), and **feature-specific** components (e.g., a user profile module).

#### 2\. **Component Design**:

* Keep components **small and focused**. A single component should ideally do one thing and do it well.
* Use **presentational components** (dumb components) for UI and **container components** (smart components) for handling logic and state.

#### 3\. **Services & Dependency Injection**:

* Use **services** for logic and business rules. Services should be **singleton** and use **Dependency Injection** (DI) to provide their instances to components or other services.

#### 4\. **Testing**:

* Write **unit tests** for services, components, and utilities using **Jasmine** and **Karma**.
* Use **Angular Testing Utilities** to mock dependencies and test isolated logic.
* **End-to-end testing** using **Protractor** or **Cypress** to test the entire app in a real browser environment.

#### 5\. **Error Handling**:

* Implement **global error handling** in the Angular app to catch errors at the application level.
* Use **interceptors** to manage errors globally, especially for HTTP requests.

#### 6\. **Performance Optimization**:

* Use **OnPush ChangeDetectionStrategy** to optimize performance by limiting unnecessary checks.
* **Lazy load modules** and reduce the initial bundle size.
* Implement **caching** for frequently used data or API responses.

---

### **4\. Singleton Pattern and Angular Services**

The **Singleton** pattern ensures that a class has only one instance throughout the lifecycle of an application. Angular uses the **Dependency Injection (DI)** system to ensure that services follow the singleton pattern by default.

* **Angular’s Service Singleton**: When you provide a service in the root module (`@Injectable({ providedIn: 'root' })`), Angular will instantiate the service once and share it across the entire application. If a service is provided at a specific module level, Angular will create a new instance for that module, which can help with scoped instances.

Example:

```typescript
@Injectable({
  providedIn: 'root' // Singleton service across the app
})
export class UserService {
  constructor(private http: HttpClient) {}
}
```

By default, services in Angular are **singletons**, meaning the same instance of the service is injected into different components, ensuring shared state and behavior.


### **1\. How would you handle authentication and authorization in an Angular application? Can you explain JWT (JSON Web Tokens) and how it works with Angular?**

**Authentication and Authorization in Angular**:  
In an Angular application, authentication and authorization are typically handled in the following steps:

* **Authentication**:  
When a user logs in, the Angular app sends a request to the backend API with user credentials (e.g., username and password). If the credentials are valid, the backend generates a **JWT** (JSON Web Token) and returns it to the Angular application.

* **Storing the Token**:  
The JWT is usually stored in the **localStorage** or **sessionStorage** in the browser. This token is then included in subsequent API requests to authenticate the user.

* **Authorization**:  
Authorization ensures that the user has permission to access specific resources. Based on the role or permissions encoded within the JWT (such as `admin`, `user`, etc.), the Angular application can restrict access to certain routes or features.

**JWT (JSON Web Tokens)**:  
A JWT is a compact, URL-safe token used to represent claims between two parties (e.g., client and server). It typically contains three parts:

1. **Header**: Specifies the algorithm used to sign the token (e.g., `HS256`).
2. **Payload**: Contains the claims, which can include user information like `userId`, `role`, etc.
3. **Signature**: Ensures the integrity of the token. It's created by signing the header and payload with a secret key.

The token is sent in the `Authorization` header of HTTP requests as follows:

```http
codeAuthorization: Bearer <JWT>
```

In Angular, the token can be retrieved from storage and attached to HTTP requests using an HTTP interceptor.

### **2\. How would you handle API calls in Angular? Explain the use of `HttpClient` and how you would manage request/response handling and error handling.**

**`HttpClient`** is the Angular service used to make HTTP requests. It is part of the `@angular/common/http` module. Here's how to use it for API calls:

1. **Import `HttpClient`**:

   ```typescript
   import  { HttpClient } from '@angular/common/http';
   import { Injectable } from '@angular/core';
   ```

2. **Inject `HttpClient` into the Service**:

   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class ApiService {
     constructor(private http: HttpClient) {}

     getData() {
       return this.http.get('https://api.example.com/data');
     }

     postData(data: any) {
       return this.http.post('https://api.example.com/data', data);
     }
   }
   ```

**Request/Response Handling**:

* `HttpClient` returns **Observables**, which makes it easy to work with asynchronous data. You can use `.subscribe()` to handle the response and handle errors in the subscription.

Example:

```typescript
codethis.apiService.getData().subscribe(
  (response) => {
    console.log('Data received', response);
  },
  (error) => {
    console.error('Error occurred', error);
  }
);
```

**Error Handling**:

* Angular’s `HttpClient` allows you to intercept and handle errors through the `.catchError()` operator or by using global HTTP interceptors.

You can also handle HTTP errors with:

```typescript
codethis.http.get('url').pipe(
  catchError((error) => {
    // Handle error, log it, or show an alert
    console.error('Request failed', error);
    return throwError(error);  // rethrow the error if needed
  })
);
```


### 1\. Common Security Concerns in Angular Applications and Mitigation

**Common Security Concerns:**

* **Cross-Site Scripting (XSS):** This occurs when an attacker injects malicious scripts into web pages viewed by other users. It can lead to session hijacking, data theft, or defacement.

* **Cross-Site Request Forgery (CSRF):** CSRF attacks trick users into making unwanted requests on websites where they are authenticated, potentially leading to actions like changing account settings or making transactions without the user's consent.

* **Insecure API Communication:** If the API is not properly secured, sensitive data might be intercepted by attackers. This includes issues like insufficient encryption (not using HTTPS) or improper authentication/authorization.

* **Insecure Dependency Management:** Including outdated or vulnerable libraries can open doors for exploits. If dependencies aren't managed properly, an attacker might target vulnerabilities in third-party code.

**Mitigation Strategies:**

* **XSS Prevention:**

  * **Sanitize Input:** Angular automatically sanitizes untrusted input by using built-in mechanisms (e.g., `{{ expression }}` in templates ensures automatic escaping). For situations requiring dynamic content, use Angular's `DomSanitizer` service to sanitize HTML, URLs, and other dangerous content.
  * **Use Angular's Security Features:** Angular has built-in protections like **sanitization**, **escaping**, and **strict Content Security Policy (CSP)** headers.
  * **Avoid `innerHTML` binding:** Instead of using `innerHTML`, use Angular's built-in safe mechanisms like `ng-bind` or property binding to avoid XSS risks.

* **CSRF Prevention:**

  * **Use Anti-CSRF Tokens:** Angular does not have a built-in CSRF protection mechanism, but it's important to implement anti-CSRF tokens on your backend (e.g., a token sent with each request to verify that the request is legitimate).
  * **SameSite Cookies:** Use cookies with the `SameSite` attribute set to `Strict` or `Lax` to prevent CSRF from cross-site requests.
  * **Ensure Safe HTTP Headers:** Ensure that the backend checks for an authentication token (JWT, OAuth) in every request header and validates the user session properly.

* **Insecure API Communication:**

  * **Always use HTTPS:** Encrypt all communication with HTTPS to prevent man-in-the-middle (MITM) attacks.
  * **Token-based Authentication:** Use JWT (JSON Web Tokens), OAuth2, or similar mechanisms to secure API endpoints.
  * **Role-Based Authorization:** Ensure that your API enforces strict access controls. The frontend should never directly manipulate access control rules.

* **Dependency Management:**

  * **Regularly Update Dependencies:** Regularly audit and update dependencies, using tools like `npm audit` to detect known vulnerabilities.
  * **Avoid Vulnerable Libraries:** Prefer libraries that are actively maintained and have minimal dependencies.
  * **Lock Dependencies:** Use `npm` or `yarn` lockfiles to ensure that all developers and build pipelines are using the same version of a dependency.

---

### 2\. Angular's Prevention of Cross-Site Scripting (XSS)

**How Angular Prevents XSS:**

* **Automatic HTML Escaping:** Angular’s template system automatically escapes any expressions that are interpolated using double curly braces (`{{ }}`). This prevents any user-supplied input from being executed as JavaScript in the browser.

  For example:

  ```html
  <div>{{ userInput }}</div>
  ```

  In the above case, Angular will escape any special characters like `<`, `>`, and `&` in the `userInput` string, rendering them as plain text rather than as HTML or script.

* **Sanitization in Bindings:** Angular automatically sanitizes untrusted input for properties like `href`, `src`, and `style`. If you use Angular's **property binding**, Angular will sanitize any dynamic URLs or styles to prevent malicious content from being injected.

* **DomSanitizer Service:** If you need to bind potentially unsafe content (e.g., HTML) in a controlled way, you can use Angular's `DomSanitizer` service to sanitize the content explicitly. For instance:

  ```typescript
  import  { DomSanitizer, SafeHtml } from '@angular/platform-browser';

  export class SafeHtmlComponent {
    constructor(private sanitizer: DomSanitizer) {}

    sanitizeHtml(dirty: string): SafeHtml {
      return this.sanitizer.bypassSecurityTrustHtml(dirty);
    }
  }
  ```

  However, you should use this service sparingly and only when you are sure the input is safe.

---

### 3\. Securing an Angular Application in a Production Environment

**Steps for Securing Angular Applications:**

1. **Enable HTTPS:**

   * Ensure that all communication between the client and server is encrypted by using HTTPS (SSL/TLS). This protects data integrity and confidentiality.

2. **Minify and Obfuscate Code:**

   * Angular’s production build (`ng build --prod`) will automatically minify and uglify the JavaScript files to make it harder for attackers to reverse-engineer the code.

3. **Set Up Content Security Policy (CSP):**

   * Configure a strict Content Security Policy to prevent inline scripts and mitigate risks like XSS. For example:
     ```json
     codeContent-Security-Policy: default-src 'self'; script-src 'self'; style-src 'self' 'unsafe-inline'; object-src 'none'; base-uri 'self';
     ```
   * This policy helps ensure that only trusted sources can execute JavaScript.

4. **Use Angular Security Features:**

   * Angular has built-in protections against XSS, so using Angular’s default mechanisms (e.g., `{{ expression }}` for data binding) significantly reduces the risk of XSS attacks.

5. **Secure API Communication:**

   * **Use OAuth2 or JWT:** For authenticating and authorizing users, use secure token-based mechanisms like OAuth2 or JWT (JSON Web Tokens) to protect API endpoints.
   * **Secure Cookie Attributes:** Use `HttpOnly`, `Secure`, and `SameSite` attributes on cookies to prevent client-side scripts from accessing sensitive session information and mitigate CSRF.
   * **Rate Limiting and Throttling:** Protect your APIs from abuse by limiting the rate of requests from individual users or IP addresses.

6. **Implement Strong Authentication and Authorization:**

   * Use multi-factor authentication (MFA) for critical operations.
   * Apply role-based access control (RBAC) or attribute-based access control (ABAC) on the backend to ensure that users can only access resources they are authorized to.

7. **Regularly Update Dependencies:**

   * Keep Angular, third-party libraries, and dependencies up-to-date by regularly auditing and patching known vulnerabilities using `npm audit` or other tools.

8. **Server-Side Security:**

   * Validate all inputs and ensure proper sanitization on the server-side.
   * Avoid relying solely on client-side validation, as attackers can bypass it.

By following these steps, you can significantly reduce the attack surface and improve the security of an Angular application in production.


### **5\. What is Ahead-of-Time (AOT) compilation, and how does it differ from Just-in-Time (JIT) compilation?**

**Ahead-of-Time (AOT)** compilation is a build-time process where the Angular template and components are precompiled before the browser even downloads the application. It transforms TypeScript and HTML into efficient JavaScript code that can be run by the browser directly.

* **AOT Compilation**:

  * **Compilation** happens during the build phase.
  * **Faster loading** since the templates are precompiled and there’s no need to do additional processing at runtime.
  * **Smaller bundle size** because unnecessary code is removed during the build process (tree-shaking).
  * **Error detection** is done earlier, since Angular can catch template errors at compile-time.
  * **Improved performance**: The app starts up faster in the browser because Angular doesn’t need to compile templates during runtime.

* **Just-in-Time (JIT)** compilation:

  * **Compilation** happens at runtime, i.e., when the application is loaded in the browser.
  * **Slower initial load time** because the browser must compile templates as the app is loaded.
  * **Larger bundle size** because the compiler and some other runtime dependencies are included in the final bundle.
  * **Easier development** since you don’t need a separate build process, but can directly work with templates and components.

* **Differences**:

  * **AOT** is generally used for production builds to improve performance and loading times, while **JIT** is used during development for faster iteration and debugging since it allows for changes to be seen immediately without requiring a rebuild.

  ### 2\. **What are some of the most challenging problems you’ve faced while working with Angular, and how did you solve them?**

Some of the most challenging problems I’ve encountered in Angular development include:

* **Performance Issues with Large Data Sets**: When working with large data sets or highly dynamic user interfaces, Angular’s change detection can sometimes become a performance bottleneck. In one instance, I worked on an application that displayed real-time data from multiple sources. The UI was slow to update when there were thousands of items in the DOM. To resolve this, I utilized techniques like **OnPush change detection strategy**, which ensures that Angular only checks components when their inputs change, significantly reducing the number of checks. I also implemented **virtual scrolling** (via Angular CDK) to render only the visible portion of the data.

* **Memory Leaks**: In a few projects, I had issues with memory leaks when components that subscribed to observables were not properly cleaned up. I solved this by leveraging the `takeUntil` operator to unsubscribe from observables when a component is destroyed. Additionally, I started using Angular's built-in `ngOnDestroy` lifecycle hook more rigorously, and I also employed the `async` pipe, which handles subscriptions automatically and avoids manual management.

* **Cross-Browser Compatibility**: Ensuring that an Angular app works consistently across all browsers can be tricky, especially with legacy browsers. In one project, I ran into issues with older versions of Internet Explorer (IE11). After thorough testing, I used **polyfills** (like those provided in Angular’s default configuration) to ensure compatibility. Additionally, I implemented fallbacks for newer CSS features and JavaScript APIs that IE11 didn’t support.

* **State Management Complexity**: As applications grow, managing state across multiple components becomes complex. I’ve worked with **NgRx** (Redux-inspired state management) in large-scale Angular applications to handle complex state transitions. One of the biggest challenges was avoiding performance bottlenecks due to excessive store updates, which I overcame by using **memoized selectors** and optimizing the number of store subscriptions.

### 3\. **How do you stay up to date with new releases and changes in the Angular framework?**

Staying up to date with Angular is critical because the framework evolves quickly. Here’s how I keep myself informed:

* **Official Angular Blog and Changelog**: The [Angularblog]() and the official changelog are essential resources. They provide release notes and important updates directly from the Angular team.

* **Angular GitHub Repository**: I regularly check the [AngularGitHubrepository](https://github.com/angular/angular) for new pull requests, issues, and discussions. This helps me stay informed about new features, bug fixes, and best practices, and also allows me to engage with the Angular community.

* **Angular Meetups and Conferences**: I attend Angular-focused conferences (e.g., AngularConnect, ng-conf) and meetups, either virtually or in person. These events often feature talks by core Angular developers and community members, and they provide a deeper understanding of new features and evolving patterns.

* **Podcasts, Newsletters, and Blogs**: I follow Angular-related podcasts, newsletters (like [ng\-newsletter](https://www.ng-newsletter.com/)), and blogs by prominent developers in the community. Listening to podcasts like "Angular Show" and reading posts from developers on platforms like Medium and Dev.to helps me get insights into best practices, performance optimizations, and new tools.

* **Experimenting with New Features**: Whenever Angular releases a major update, I try to create side projects or contribute to open-source projects that adopt these new features. This hands-on approach helps me understand the practical implications of new releases.

### 4\. **Can you walk us through a specific project where you applied Angular to solve a complex problem? What were the challenges, and how did you address them?**

One project that stands out involved building a **real-time data dashboard** for a logistics company, where users needed to track thousands of shipments and their statuses in real-time. The challenges were mainly around performance, state management, and real-time updates.

* **Challenge 1: Handling Real-Time Data**: The application had to handle frequent data updates from multiple sources (e.g., GPS updates, status changes). The challenge was ensuring that the UI remained responsive while updating the data efficiently. I used **WebSockets** for real-time communication, and implemented **RxJS operators** like `debounceTime`, `distinctUntilChanged`, and `switchMap` to manage the flow of real-time data and avoid unnecessary re-renders.

* **Challenge 2: Performance with Large Data Sets**: The dashboard needed to display thousands of records, which created performance issues when loading the entire dataset at once. I solved this by implementing **lazy loading** and **virtual scrolling** for the tables. Only the visible data was rendered, which significantly improved performance. I also optimized the API to fetch data in chunks based on the viewport.

* **Challenge 3: State Management**: The app’s state was complex, with a need to sync user interactions (e.g., filtering and sorting) with real-time updates. I chose **NgRx** for state management to centralize all app states and avoid inconsistent UI states. By using **selectors** and **effects** in NgRx, I was able to efficiently manage asynchronous operations and ensure the UI reflected the most up-to-date data.

* **Challenge 4: Cross-Browser Compatibility**: The app needed to work across a range of browsers, including legacy versions of Internet Explorer. To solve this, I configured Webpack with additional polyfills and used CSS fallbacks to ensure that the app looked and worked well in all browsers.

-------------------------
-------------------------

9. ### What is a template?
    A template is a HTML view where you can display data by binding controls to properties of an Angular component. You can store your component's template in one of two places. You can define it inline using the template property, or you can define the template in a separate HTML file and link to it in the component metadata using the @Component decorator's templateUrl property.

    **Using inline template with template syntax,**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       template: '
          <div>
             <h1>{{title}}</h1>
             <div>Learn Angular</div>
          </div>
       '
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```
    **Using separate template file such as app.component.html**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       templateUrl: 'app/app.component.html'
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

12. ### What is a data binding?
    Data binding is a core concept in Angular and allows to define communication between a component and the DOM, making it very easy to define interactive applications without worrying about pushing and pulling data. There are four forms of data binding(divided as 3 categories) which differ in the way the data is flowing.
    1. **From the Component to the DOM:**

        **Interpolation:** {{ value }}: Adds the value of a property from the component
        ```html
        <li>Name: {{ user.name }}</li>
        <li>Address: {{ user.address }}</li>
        ```
        **Property binding:** [property]=”value”: The value is passed from the component to the specified property or simple HTML attribute
        ```html
        <input type="email" [value]="user.email">
        ```
    2. **From the DOM to the Component:**
        **Event binding: (event)=”function”:** When a specific DOM event happens (eg.: click, change, keyup), call the specified method in the component
        ```html
        <button (click)="logout()"></button>
        ```
    3. **Two-way binding:**
        **Two-way data binding:** [(ngModel)]=”value”: Two-way data binding allows to have the data flow both ways. For example, in the below code snippet, both the email DOM input and component email property are in sync
        ```html
        <input type="email" [(ngModel)]="user.email">
        ```

  **[⬆ Back to Top](#table-of-contents)**

13. ### What is metadata?
    Metadata is used to decorate a class so that it can configure the expected behavior of the class. The metadata is represented by decorators
    1. **Class decorators**, e.g. @Component and @NgModule
        ```typescript
        import { NgModule, Component } from '@angular/core';

        @Component({
          selector: 'my-component',
          template: '<div>Class decorator</div>',
        })
        export class MyComponent {
          constructor() {
            console.log('Hey I am a component!');
          }
        }

        @NgModule({
          imports: [],
          declarations: [],
        })
        export class MyModule {
          constructor() {
            console.log('Hey I am a module!');
          }
        }
        ```
    2. **Property decorators** Used for properties inside classes, e.g. @Input and @Output
        ```typescript
        import { Component, Input } from '@angular/core';

        @Component({
            selector: 'my-component',
            template: '<div>Property decorator</div>'
        })

        export class MyComponent {
            @Input()
            title: string;
        }
        ```
    3. **Method decorators** Used for methods inside classes, e.g. @HostListener
        ```typescript
        import { Component, HostListener } from '@angular/core';

        @Component({
            selector: 'my-component',
            template: '<div>Method decorator</div>'
        })
        export class MyComponent {
            @HostListener('click', ['$event'])
            onHostClick(event: Event) {
                // clicked, `event` available
            }
        }
        ```
    4. **Parameter decorators** Used for parameters inside class constructors, e.g. @Inject, @Optional
        ```typescript
        import { Component, Inject } from '@angular/core';
        import { MyService } from './my-service';

        @Component({
            selector: 'my-component',
            template: '<div>Parameter decorator</div>'
        })
        export class MyComponent {
            constructor(@Inject(MyService) myService) {
                console.log(myService); // MyService
            }
        }
        ```
  **[⬆ Back to Top](#table-of-contents)**

14. ### What is angular CLI?
    Angular CLI(**Command Line Interface**) is a command line interface to scaffold and build angular apps using nodejs style (commonJs) modules.
    You need to install using below npm command,
    ```
    npm install @angular/cli@latest
    ```
    Below are the list of few commands, which will come handy while creating angular projects
    1. **Creating New Project:** ng new <project-name>

    2. **Generating Components, Directives & Services:** ng generate/g <feature-name>
        The different types of commands would be,
        * ng generate class my-new-class: add a class to your application
        * ng generate component my-new-component: add a component to your application
        * ng generate directive my-new-directive: add a directive to your application
        * ng generate enum my-new-enum: add an enum to your application
        * ng generate module my-new-module: add a module to your application
        * ng generate pipe my-new-pipe: add a pipe to your application
        * ng generate service my-new-service: add a service to your application

    3. **Running the Project:** ng serve

  **[⬆ Back to Top](#table-of-contents)**

15. ### What is the difference between constructor and ngOnInit?
    The **Constructor** is a default method of the class that is executed when the class is instantiated and ensures proper initialisation of fields in the class and its subclasses. Angular, or better Dependency Injector (DI), analyses the constructor parameters and when it creates a new instance by calling new MyClass() it tries to find providers that match the types of the constructor parameters, resolves them and passes them to the constructor.  
    **ngOnInit** is a life cycle hook called by Angular to indicate that Angular is done creating the component.  
    Mostly we use ngOnInit for all the initialization/declaration and avoid stuff to work in the constructor. The constructor should only be used to initialize class members but shouldn't do actual "work".
    So you should use constructor() to setup Dependency Injection and not much else. ngOnInit() is better place to "start" - it's where/when components' bindings are resolved.

    ```typescript
    export class App implements OnInit{
      constructor(private myService: MyService){
         //called first time before the ngOnInit()
      }

      ngOnInit(){
         //called after the constructor and called  after the first ngOnChanges()
         //e.g. http call...
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

18. ### How is Dependency Hierarchy formed?
    Injectors in Angular have rules that can be leveraged to achieve the desired visibility of injectables in your applications. By understanding these rules, you can determine in which NgModule, Component, or Directive you should declare a provider.

    #### Angular has two injector hierarchies:
    ![Screenshot](/images/injector%20hierarchies.png)

    #### Module injector 
    When angular starts, it creates a root injector where the services will be registered, these are provided via injectable annotation. All services provided in the `ng-model` property are called providers (if those modules are not lazy-loaded).

    Angular recursively goes through all models which are being used in the application and creates instances for provided services in the root injector. If you provide some service in an eagerly-loaded model, the service will be added to the root injector, which makes it available across the whole application.

    #### Platform Module
    During application bootstrapping angular creates a few more injectors, above the root injector goes the platform injector, this one is created by the platform browser dynamic function inside the `main.ts` file, and it provides some platform-specific features like `DomSanitizer`. 

    #### NullInjector()
    At the very top, the next parent injector in the hierarchy is the `NullInjector()`.The responsibility of this injector is to throw the error if something tries to find dependencies there, unless you've used `@Optional()` because ultimately, everything ends at the `NullInjector()` and it returns an error or, in the case of `@Optional()`, `null`.

    ![Screenshot](images/hierarchy%20diagram.png)


    #### ElementInjector
    Angular creates `ElementInjector` hierarchies implicitly for each DOM element. `ElementInjector` injector is being created for any tag that matches the angular component, or any tag on which directive is applied, and you can configure it in component and directive annotations inside the provider's property, thus, it creates its own hierarchy likewise the upper one.

    ![Screenshot](images/element%20injector%20hieracrhy.png)

  **[⬆ Back to Top](#table-of-contents)**

19. ### What is the purpose of async pipe?
    The AsyncPipe subscribes to an observable or promise and returns the latest value it has emitted. When a new value is emitted, the pipe marks the component to be checked for changes.

    Let's take a time observable which continuously updates the view for every 2 seconds with the current time.
    ```typescript
    @Component({
      selector: 'async-observable-pipe',
      template: `<div><code>observable|async</code>:
           Time: {{ time | async }}</div>`
    })
    export class AsyncObservablePipeComponent {
      time: Observable<string>;
      constructor() {
        this.time = new Observable((observer) => {
          setInterval(() => {
            observer.next(new Date().toString());
          }, 2000);
        });
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

20. ### What is the option to choose between inline and external template file?
    You can store your component's template in one of two places. You can define it inline using the **template** property, or you can define the template in a separate HTML file and link to it in the component metadata using the **@Component** decorator's **templateUrl** property.

    The choice between inline and separate HTML is a matter of taste, circumstances, and organization policy. But normally we use inline template for small portion of code and external template file for bigger views. By default, the Angular CLI generates components with a template file. But you can override that with the below command,
    ```
    ng generate component hero -it
    ```

  **[⬆ Back to Top](#table-of-contents)**

21. ### What is the purpose of `*ngFor` directive?
    We use Angular `*ngFor` directive in the template to display each item in the list. For example, here we can iterate over a list of users:
    ```html
    <li *ngFor="let user of users">
      {{ user }}
    </li>
    ```
    The user variable in the `*ngFor` double-quoted instruction is a **template input variable**.

  **[⬆ Back to Top](#table-of-contents)**

22. ### What is the purpose of `*ngIf` directive?
    Sometimes an app needs to display a view or a portion of a view only under specific circumstances. The Angular `*ngIf` directive inserts or removes an element based on a truthy/falsy condition. Let's take an example to display a message if the user age is more than 18:
    ```html
    <p *ngIf="user.age > 18">You are not eligible for student pass!</p>
    ```
    **Note:** Angular isn't showing and hiding the message. It is adding and removing the paragraph element from the DOM. That improves performance, especially in the larger projects with many data bindings.

  **[⬆ Back to Top](#table-of-contents)**

23. ### What happens if you use script tag inside template?

    Angular recognizes the value as unsafe and automatically sanitizes it, which removes the `script` tag but keeps safe content such as the text content of the `script` tag. This way it eliminates the risk of script injection attacks. If you still use it then it will be ignored and a warning appears in the browser console.

    Let's take an example of innerHtml property binding which causes XSS vulnerability,
    ```typescript
    export class InnerHtmlBindingComponent {
      // For example, a user/attacker-controlled value from a URL.
      htmlSnippet = 'Template <script>alert("0wned")</script> <b>Syntax</b>';
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

24. ### What is interpolation?

    Interpolation is a special syntax that Angular converts into property binding. It’s a convenient alternative to property binding. It is represented by double curly braces({{}}). The text between the braces is often the name of a component property. Angular replaces that name with the string value of the corresponding component property.

    Let's take an example,
    ```html
    <h3>
      {{title}}
      <img src="{{url}}" style="height:30px">
    </h3>
    ```
    In the example above, Angular evaluates the title and url properties and fills in the blanks, first displaying a bold application title and then a URL.

  **[⬆ Back to Top](#table-of-contents)**

25. ### What are template expressions?
    A template expression produces a value similar to any Javascript expression. Angular executes the expression and assigns it to a property of a binding target; the target might be an HTML element, a component, or a directive. In the property binding, a template expression appears in quotes to the right of the = symbol as in `[property]="expression"`.
    In interpolation syntax, the template expression is surrounded by double curly braces. For example, in the below interpolation, the template expression is `{{username}}`,

    ```html
    <h3>{{username}}, welcome to Angular</h3>
    ```

    The below javascript expressions are prohibited in template expression
    1. assignments (=, +=, -=, ...)
    2. new
    3. chaining expressions with ; or ,
    4. increment and decrement operators (++ and --)
    ----------------------------------

  **[⬆ Back to Top](#table-of-contents)**

26. ### What are template statements?
    A template statement responds to an event raised by a binding target such as an element, component, or directive. The template statements appear in quotes to the right of the = symbol like `(event)="statement"`.

    Let's take an example of button click event's statement

    ```html
    <button (click)="editProfile()">Edit Profile</button>
    ```
    In the above expression, editProfile is a template statement. The below JavaScript syntax expressions are not allowed.
    1. new
    2. increment and decrement operators, ++ and --
    3. operator assignment, such as += and -=
    4. the bitwise operators | and &
    5. the template expression operators
    --------------------------------------

  **[⬆ Back to Top](#table-of-contents)**

27. ### How do you categorize data binding types?

     Binding types can be grouped into three categories distinguished by the direction of data flow. They are listed as below,
     1. From the source-to-view
     2. From view-to-source
     3. View-to-source-to-view

     The possible binding syntax can be tabularized as below,

      | Data direction | Syntax | Type |
      |---- | --------- | ---- |
      | From the source-to-view(One-way)  | 1. {{expression}} 2. [target]="expression" 3. bind-target="expression" | Interpolation, Property, Attribute, Class, Style|
      | From view-to-source(One-way) | 1. (target)="statement" 2. on-target="statement" | Event |
      | View-to-source-to-view(Two-way)| 1. [(target)]="expression" 2. bindon-target="expression"| Two-way |

  **[⬆ Back to Top](#table-of-contents)**

29. ### What is a parameterized pipe?
    A pipe can accept any number of optional parameters to fine-tune its output. The parameterized pipe can be created by declaring the pipe name with a colon ( : ) and then the parameter value. If the pipe accepts multiple parameters, separate the values with colons. Let's take a birthday example with a particular format(dd/MM/yyyy):

    ```javascript
    import { Component } from '@angular/core';

        @Component({
          selector: 'app-birthday',
          template: `<p>Birthday is {{ birthday | date:'dd/MM/yyyy'}}</p>` // 18/06/1987
        })
        export class BirthdayComponent {
          birthday = new Date(1987, 6, 18);
        }
    ```
    **Note:** The parameter value can be any valid template expression, such as a string literal or a component property.

  **[⬆ Back to Top](#table-of-contents)**

30. ### How do you chain pipes?
    You can chain pipes together in potentially useful combinations as per the needs. Let's take a birthday property which uses date pipe(along with parameter) and uppercase pipes as below

    ```javascript
    import { Component } from '@angular/core';

            @Component({
              selector: 'app-birthday',
              template: `<p>Birthday is {{  birthday | date:'fullDate' | uppercase}} </p>` // THURSDAY, JUNE 18, 1987
            })
            export class BirthdayComponent {
              birthday = new Date(1987, 6, 18);
            }

    ```

  **[⬆ Back to Top](#table-of-contents)**

31. ### What is a custom pipe?
    Apart from built-in pipes, you can write your own custom pipe with the below key characteristics:
    1. A pipe is a class decorated with pipe metadata `@Pipe` decorator, which you import from the core Angular library
       For example,
        ```javascript
            @Pipe({name: 'myCustomPipe'})
        ```
    2. The pipe class implements the **PipeTransform** interface's transform method that accepts an input value followed by optional parameters and returns the transformed value.
       The structure of `PipeTransform` would be as below,
        ```javascript
        interface PipeTransform {
          transform(value: any, ...args: any[]): any
        }
        ```
    3. The `@Pipe` decorator allows you to define the pipe name that you'll use within template expressions. It must be a valid JavaScript identifier.
        ```javascript
        template: `{{someInputValue | myCustomPipe: someOtherValue}}`
        ```

  **[⬆ Back to Top](#table-of-contents)**

32. ### Give an example of custom pipe?
    You can create custom reusable pipes for the transformation of existing value. For example, let us create a custom pipe for finding file size based on an extension,
      ```javascript
        import { Pipe, PipeTransform } from '@angular/core';

        @Pipe({name: 'customFileSizePipe'})
        export class FileSizePipe implements PipeTransform {
          transform(size: number, extension: string = 'MB'): string {
            return (size / (1024 * 1024)).toFixed(2) + extension;
          }
        }
      ```
    Now you can use the above pipe in template expression as below,
      ```javascript
         template: `
            <h2>Find the size of a file</h2>
            <p>Size: {{288966 | customFileSizePipe: 'GB'}}</p>
          `
      ```

  **[⬆ Back to Top](#table-of-contents)**

33. ### What is the difference between pure and impure pipe?
    A pure pipe is only called when Angular detects a change in the value or the parameters passed to a pipe. For example, any changes to a primitive input value (String, Number, Boolean, Symbol) or a changed object reference (Date, Array, Function, Object). An impure pipe is called for every change detection cycle no matter whether the value or parameters changes. i.e, An impure pipe is called often, as often as every keystroke or mouse-move.

  **[⬆ Back to Top](#table-of-contents)**

36. ### What is HttpClient and its benefits?
    Most of the Front-end applications communicate with backend services over `HTTP` protocol using either `XMLHttpRequest` interface or the `fetch()` API. Angular provides a simplified client HTTP API known as `HttpClient` which is based on top of `XMLHttpRequest` interface. This client is available from `@angular/common/http` package.
    You can import in your root module as below:

    ```javascript
    import { HttpClientModule } from '@angular/common/http';
    ```

    The major advantages of HttpClient can be listed as below,
    1. Contains testability features
    2. Provides typed request and response objects
    3. Intercept request and response
    4. Supports Observable APIs
    5. Supports streamlined error handling

  **[⬆ Back to Top](#table-of-contents)**

37. ### Explain on how to use `HttpClient` with an example?
    Below are the steps need to be followed for the usage of `HttpClient`.
    1. Import `HttpClient` into root module:
        ```javascript
        import { HttpClientModule } from '@angular/common/http';
        @NgModule({
          imports: [
            BrowserModule,
            // import HttpClientModule after BrowserModule.
            HttpClientModule,
          ],
          ......
          })
         export class AppModule {}
        ```
    2. Inject the `HttpClient` into the application:
        Let's create a userProfileService(`userprofile.service.ts`) as an example. It also defines get method of `HttpClient`:
        ```javascript
        import { Injectable } from '@angular/core';
        import { HttpClient } from '@angular/common/http';

        const userProfileUrl: string = 'assets/data/profile.json';

        @Injectable()
        export class UserProfileService {
          constructor(private http: HttpClient) { }

          getUserProfile() {
            return this.http.get(this.userProfileUrl);
          }
        }
        ```
    3. Create a component for subscribing service:
        Let's create a component called UserProfileComponent(`userprofile.component.ts`), which injects `UserProfileService` and invokes the service method:
        ```javascript
        fetchUserProfile() {
          this.userProfileService.getUserProfile()
            .subscribe((data: User) => this.user = {
                id: data['userId'],
                name: data['firstName'],
                city:  data['city']
            });
        }
        ```
    Since the above service method returns an Observable which needs to be subscribed in the component.

  **[⬆ Back to Top](#table-of-contents)**

38. ### How can you read full response?
    The response body doesn't or may not return full response data because sometimes servers also return special headers or status code, which are important for the application workflow. In order to get the full response, you should use `observe` option from `HttpClient`:

    ```javascript
    getUserResponse(): Observable<HttpResponse<User>> {
      return this.http.get<User>(
        this.userUrl, { observe: 'response' });
    }
    ```
    Now `HttpClient.get()` method returns an Observable of typed `HttpResponse` rather than just the `JSON` data.

  **[⬆ Back to Top](#table-of-contents)**

39. ### How do you perform Error handling?
    If the request fails on the server or fails to reach the server due to network issues, then `HttpClient` will return an error object instead of a successful response. In this case, you need to handle in the component by passing `error` object as a second callback to `subscribe()` method.

    Let's see how it can be handled in the component with an example,
    ```javascript
    fetchUser() {
      this.userService.getProfile()
        .subscribe(
          (data: User) => this.userProfile = { ...data }, // success path
          error => this.error = error // error path
        );
    }
    ```
    It is always a good idea to give the user some meaningful feedback instead of displaying the raw error object returned from `HttpClient`.

  **[⬆ Back to Top](#table-of-contents)**

46. ### How do you perform error handling in observables?
    You can handle errors by specifying an **error callback** on the observer instead of relying on `try`/`catch`, which are ineffective in asynchronous environment.

    For example, you can define error callback as below,
    ```javascript
    myObservable.subscribe({
      next(num) { console.log('Next num: ' + num)},
      error(err) { console.log('Received an error: ' + err)}
    });
    ```

  **[⬆ Back to Top](#table-of-contents)**

47. ### What is the shorthand notation for subscribe method?
    The `subscribe()` method can accept callback function definitions in line, for `next`, `error`, and `complete` handlers. It is known as shorthand notation or Subscribe method with positional arguments.

    For example, you can define subscribe method as below,
    ```javascript
    myObservable.subscribe(
      x => console.log('Observer got a next value: ' + x),
      err => console.error('Observer got an error: ' + err),
      () => console.log('Observer got a complete notification')
    );
    ```

  **[⬆ Back to Top](#table-of-contents)**

48. ### What are the utility functions provided by RxJS?
    The RxJS library also provides below utility functions for creating and working with observables.

    1. Converting existing code for async operations into observables
    2. Iterating through the values in a stream
    3. Mapping values to different types
    4. Filtering streams
    5. Composing multiple streams

  **[⬆ Back to Top](#table-of-contents)**

49. ### What are observable creation functions?
    RxJS provides creation functions for the process of creating observables from promises, events, timers and Ajax requests. Let us explain each of them with an example:
    1. Create an observable from a promise
        ```javascript
        import { from } from 'rxjs'; // from function
        const data = from(fetch('/api/endpoint')); //Created from Promise
        data.subscribe({
         next(response) { console.log(response); },
         error(err) { console.error('Error: ' + err); },
         complete() { console.log('Completed'); }
        });
        ```
    2. Create an observable that creates an AJAX request
        ```javascript
        import { ajax } from 'rxjs/ajax'; // ajax function
        const apiData = ajax('/api/data'); // Created from AJAX request
        // Subscribe to create the request
        apiData.subscribe(res => console.log(res.status, res.response));
        ```
    3. Create an observable from a counter
        ```javascript
        import { interval } from 'rxjs'; // interval function
        const secondsCounter = interval(1000); // Created from Counter value
        secondsCounter.subscribe(n =>
          console.log(`Counter value: ${n}`));
        ```
    4. Create an observable from an event
        ```javascript
        import { fromEvent } from 'rxjs';
        const el = document.getElementById('custom-element');
        const mouseMoves = fromEvent(el, 'mousemove');
        const subscription = mouseMoves.subscribe((e: MouseEvent) => {
          console.log(`Coordnitaes of mouse pointer: ${e.clientX} * ${e.clientY}`);
          });
        ```

  **[⬆ Back to Top](#table-of-contents)**

50. ### What will happen if you do not supply handler for the observer?
    Usually, an observer object can define any combination of `next`, `error`, and `complete` notification type handlers. If you don't supply a handler for a notification type, the observer just ignores notifications of that type.

  **[⬆ Back to Top](#table-of-contents)**

51. ### What are Angular elements?
    Angular elements are Angular components packaged as **custom elements** (a web standard for defining new HTML elements in a framework-agnostic way). Angular Elements host an Angular component, providing a bridge between the data and the logic defined in the component and the standard DOM APIs, thus, providing a way to use Angular components in `non-Angular environments`.

  **[⬆ Back to Top](#table-of-contents)**

52. ### What is the browser support of Angular Elements?
    Since Angular elements are packaged as custom elements the browser support of angular elements is same as custom elements support.

    This feature is is currently supported natively in a number of browsers and pending for other browsers.

    | Browser | Angular Element Support |
    |---- | --------- |
    | Chrome | Natively supported|
    | Opera | Natively supported |
    | Safari| Natively supported |
    | Firefox | Natively supported from 63 version onwards. You need to enable dom.webcomponents.enabled and dom.webcomponents.customelements.enabled in older browsers |
    | Edge| Currently it is in progress|

  **[⬆ Back to Top](#table-of-contents)**

53. ### What are custom elements?
    Custom elements (or Web Components) are a Web Platform feature which extends HTML by allowing you to define a tag whose content is created and controlled by JavaScript code. The browser maintains a `CustomElementRegistry` of defined custom elements, which maps an instantiable JavaScript class to an HTML tag. Currently this feature is supported by Chrome, Firefox, Opera, and Safari, and available in other browsers through polyfills.

  **[⬆ Back to Top](#table-of-contents)**

54. ### Do I need to bootstrap custom elements?
    No, custom elements bootstrap (or start) automatically when they are added to the DOM, and are automatically destroyed when removed from the DOM. Once a custom element is added to the DOM for any page, it looks and behaves like any other HTML element, and does not require any special knowledge of Angular.

  **[⬆ Back to Top](#table-of-contents)**

55. ### Explain how custom elements works internally?
    Below are the steps in an order about custom elements functionality,
    1. **App registers custom element with browser:** Use the `createCustomElement()` function to convert a component into a class that can be registered with the browser as a custom element.
    2. **App adds custom element to DOM:**  Add custom element just like a built-in HTML element directly into the DOM.
    3. **Browser instantiate component based class:** Browser creates an instance of the registered class and adds it to the DOM.
    4. **Instance provides content with data binding and change detection:** The content with in template is rendered using the component and DOM data.
    The flow chart of the custom elements functionality would be as follows,

    ![CustomElement](images/customElement.png)

  **[⬆ Back to Top](#table-of-contents)**

56. ### How to transfer components to custom elements?
    Transforming components to custom elements involves **two** major steps,
    1. **Build custom element class:** Angular provides the `createCustomElement()` function for converting an Angular component (along with its dependencies) to a custom element. The conversion process implements `NgElementConstructor` interface, and creates a constructor class which is used to produce a self-bootstrapping instance of Angular component.
    2. **Register element class with browser:** It uses `customElements.define()` JS function, to register the configured constructor and its associated custom-element tag with the browser's `CustomElementRegistry`. When the browser encounters the tag for the registered element, it uses the constructor to create a custom-element instance.

    The detailed structure would be as follows,
    ![CreateElement](images/createElement.png)

  **[⬆ Back to Top](#table-of-contents)**

57. ### What are the mapping rules between Angular component and custom element?
    The Component properties and logic maps directly into HTML attributes and the browser's event system. Let us describe them in two steps,
    1. The createCustomElement() API parses the component input properties with corresponding attributes for the custom element. For example, component @Input('myInputProp') converted as custom element attribute `my-input-prop`.
    2. The Component outputs are dispatched as HTML Custom Events, with the name of the custom event matching the output name. For example, component @Output() valueChanged = new EventEmitter() converted as custom element with dispatch event as "valueChanged".

  **[⬆ Back to Top](#table-of-contents)**

58. ### How do you define typings for custom elements?
    You can use the `NgElement` and `WithProperties` types exported from @angular/elements.

    Let's see how it can be applied by comparing with Angular component.
    1. The simple container with input property would be as below,
        ```javascript
        @Component(...)
        class MyContainer {
          @Input() message: string;
        }
        ```
    2. After applying types typescript validates input value and their types,
        ```javascirpt
        const container = document.createElement('my-container') as NgElement & WithProperties<{message: string}>;
        container.message = 'Welcome to Angular elements!';
        container.message = true;  // <-- ERROR: TypeScript knows this should be a string.
        container.greet = 'News';  // <-- ERROR: TypeScript knows there is no `greet` property on `container`.
        ```

  **[⬆ Back to Top](#table-of-contents)**

59. ### What are dynamic components?
    Dynamic components are the components in which the component's location in the application is not defined at build time i.e. they are not used in any angular template. Instead, the component is instantiated and placed in the application at runtime.

  **[⬆ Back to Top](#table-of-contents)**

60. ### What are the various kinds of directives?
    There are mainly three kinds of directives:
    1. **Components** — These are directives with a template.
    2. **Structural directives** — These directives change the DOM layout by adding and removing DOM elements.
    3. **Attribute directives** — These directives change the appearance or behavior of an element, component, or another directive.

  **[⬆ Back to Top](#table-of-contents)**

61. ### How do you create directives using CLI?
    You can use CLI command `ng generate directive` to create the directive class file. It creates the source file(`src/app/components/directivename.directive.ts`), the respective test file `.spec.ts` and declare the directive class file in root module.

  **[⬆ Back to Top](#table-of-contents)**

62. ### Give an example for attribute directives?
    Let's take simple highlighter behavior as a example directive for DOM element. You can create and apply the attribute directive using below step:

    1. Create HighlightDirective class with the file name `src/app/highlight.directive.ts`. In this file, we need to import **Directive** from core library to apply the metadata and **ElementRef** in the directive's constructor to inject a reference to the host DOM element ,
        ```javascript
        import { Directive, ElementRef } from '@angular/core';

        @Directive({
          selector: '[appHighlight]'
        })
        export class HighlightDirective {
            constructor(el: ElementRef) {
               el.nativeElement.style.backgroundColor = 'red';
            }
        }
        ```
    2. Apply the attribute directive as an attribute to the host element(for example, <p>)
        ```javascript
        <p appHighlight>Highlight me!</p>
        ```
    3. Run the application to see the highlight behavior on paragraph element
        ```javascript
        ng serve
        ```

  **[⬆ Back to Top](#table-of-contents)**

64. ### What is the purpose of base href tag?
    The routing application should add <base> element to the index.html as the first child in the <head> tag in order to indicate how to compose navigation URLs. If app folder is the application root then you can set the href value as below

    ```html
    <base href="/">
    ```

  **[⬆ Back to Top](#table-of-contents)**

65. ### What are the router imports?
    The Angular Router which represents a particular component view for a given URL is not part of Angular Core. It is available in library named `@angular/router` to import required router components. For example, we import them in app module as below,

    ```javascript
    import { RouterModule, Routes } from '@angular/router';
    ```

  **[⬆ Back to Top](#table-of-contents)**

66. ### What is router outlet?
    The RouterOutlet is a directive from the router library and it  acts as a placeholder that marks the spot in the template where the router should display the components for that outlet. Router outlet is used like a component,

    ```html
    <router-outlet></router-outlet>
    <!-- Routed components go here -->
    ```

  **[⬆ Back to Top](#table-of-contents)**

67. ### What are router links?
    The RouterLink is a directive on the anchor tags give the router control over those elements. Since the navigation paths are fixed, you can assign string values to router-link directive as below,

    ```html
    <h1>Angular Router</h1>
    <nav>
      <a routerLink="/todosList" >List of todos</a>
      <a routerLink="/completed" >Completed todos</a>
    </nav>
    <router-outlet></router-outlet>
    ```

  **[⬆ Back to Top](#table-of-contents)**

68. ### What are active router links?
    RouterLinkActive is a directive that toggles css classes for active RouterLink bindings based on the current RouterState. i.e, The Router will add CSS classes when this link is active and remove when the link is inactive. For example, you can add them to RouterLinks as below.

    ```html
    <h1>Angular Router</h1>
    <nav>
      <a routerLink="/todosList" routerLinkActive="active">List of todos</a>
      <a routerLink="/completed" routerLinkActive="active">Completed todos</a>
    </nav>
    <router-outlet></router-outlet>
    ```

  **[⬆ Back to Top](#table-of-contents)**

69. ### What is router state?
    RouterState is a tree of activated routes. Every node in this tree knows about the "consumed" URL segments, the extracted parameters, and the resolved data. You can access the current RouterState from anywhere in the application using the `Router service` and the `routerState` property.

    ```javascript
    @Component({templateUrl:'template.html'})
    class MyComponent {
      constructor(router: Router) {
        const state: RouterState = router.routerState;
        const root: ActivatedRoute = state.root;
        const child = root.firstChild;
        const id: Observable<string> = child.params.map(p => p.id);
        //...
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

70. ### What are router events?
    During each navigation, the Router emits navigation events through the Router.events property allowing you to track the lifecycle of the route.

    The sequence of router events is as below,

    1. NavigationStart,
    2. RouteConfigLoadStart,
    3. RouteConfigLoadEnd,
    4. RoutesRecognized,
    5. GuardsCheckStart,
    6. ChildActivationStart,
    7. ActivationStart,
    8. GuardsCheckEnd,
    9. ResolveStart,
    10. ResolveEnd,
    11. ActivationEnd
    12. ChildActivationEnd
    13. NavigationEnd,
    14. NavigationCancel,
    15. NavigationError
    16. Scroll

  **[⬆ Back to Top](#table-of-contents)**

71. ### What is activated route?
    ActivatedRoute contains the information about a route associated with a component loaded in an outlet. It can also be used to traverse the router state tree. The ActivatedRoute will be injected as a router service to access the information. In the below example, you can access route path and parameters,

    ```javascript
    @Component({...})
    class MyComponent {
      constructor(route: ActivatedRoute) {
        const id: Observable<string> = route.params.pipe(map(p => p.id));
        const url: Observable<string> = route.url.pipe(map(segments => segments.join('')));
        // route.data includes both `data` and `resolve`
        const user = route.data.pipe(map(d => d.user));
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

72. ### How do you define routes?
     A router must be configured with a list of route definitions. You configures the router with routes via the `RouterModule.forRoot()` method, and adds the result to the AppModule's `imports` array.

    ```javascript
     const appRoutes: Routes = [
      { path: 'todo/:id',      component: TodoDetailComponent },
      {
        path: 'todos',
        component: TodosListComponent,
        data: { title: 'Todos List' }
      },
      { path: '',
        redirectTo: '/todos',
        pathMatch: 'full'
      },
      { path: '**', component: PageNotFoundComponent }
    ];

    @NgModule({
      imports: [
        RouterModule.forRoot(
          appRoutes,
          { enableTracing: true } // <-- debugging purposes only
        )
        // other imports here
      ],
      ...
    })
    export class AppModule { }
    ```

   **[⬆ Back to Top](#table-of-contents)**

73. ### What is the purpose of Wildcard route?
    If the URL doesn't match any predefined routes then it causes the router to throw an error and crash the app. In this case, you can use wildcard route. A wildcard route has a path consisting of two asterisks to match every URL.

    For example, you can define PageNotFoundComponent for wildcard route as below
    ```javascript
    { path: '**', component: PageNotFoundComponent }
    ```

  **[⬆ Back to Top](#table-of-contents)**

74. ### Do I need a Routing Module always?
    No, the Routing Module is a design choice. You can skip routing Module (for example, AppRoutingModule) when the configuration is simple and merge the routing configuration directly into the companion module (for example, AppModule). But it is recommended when the configuration is complex and includes specialized guard and resolver services.

  **[⬆ Back to Top](#table-of-contents)**

75. ### What is Angular Universal?
    Angular Universal is a server-side rendering module for Angular applications in various scenarios. This is a community driven project and available under @angular/platform-server package. Recently Angular Universal is integrated with Angular CLI.

  **[⬆ Back to Top](#table-of-contents)**

76. ### What are different types of compilation in Angular?
    Angular offers two ways to compile your application,
    1. Just-in-Time (JIT)
    2. Ahead-of-Time (AOT)

  **[⬆ Back to Top](#table-of-contents)**

77. ### What is JIT?
    Just-in-Time (JIT) is a type of compilation that compiles your app in the browser at runtime. JIT compilation was the default until Angular 8, now default is AOT. When you run the ng build (build only) or ng serve (build and serve locally) CLI commands, the type of compilation (JIT or AOT) depends on the value of the aot property in your build configuration specified in angular.json. By default, aot is set to true.

  **[⬆ Back to Top](#table-of-contents)**

78. ### What is AOT?
    Ahead-of-Time (AOT) is a type of compilation that compiles your app at build time. This is the default starting in Angular 9. When you run the ng build (build only) or ng serve (build and serve locally) CLI commands, the type of compilation (JIT or AOT) depends on the value of the aot property in your build configuration specified in angular.json. By default, aot is set to true.
    
    ```cmd
    ng build
    ng serve
    ```

  **[⬆ Back to Top](#table-of-contents)**

79. ### Why do we need compilation process?
    The Angular components and templates cannot be understood by the browser directly. Due to that Angular applications require a compilation process before they can run in a browser. For example, In AOT compilation, both Angular HTML and TypeScript code converted into efficient JavaScript code during the build phase before browser runs it.

  **[⬆ Back to Top](#table-of-contents)**

80. ### What are the advantages with AOT?
    Below are the list of AOT benefits,

    1. **Faster rendering:** The browser downloads a pre-compiled version of the application. So it can render the application immediately without compiling the app.
    2. **Fewer asynchronous requests:** It inlines external HTML templates and CSS style sheets within the application javascript which eliminates separate ajax requests.
    3. **Smaller Angular framework download size:** Doesn't require downloading the Angular compiler. Hence it dramatically reduces the application payload.
    4. **Detect template errors earlier:** Detects and reports template binding errors during the build step itself
    5. **Better security:** It compiles HTML templates and components into JavaScript.  So there won't be any injection attacks.

  **[⬆ Back to Top](#table-of-contents)**

81. ### What are the ways to control AOT compilation?
    You can control your app compilation in two ways,
    1. By providing template compiler options in the `tsconfig.json` file
    2. By configuring Angular metadata with decorators

  **[⬆ Back to Top](#table-of-contents)**

82. ### What are the restrictions of metadata?
    In Angular, You must write metadata with the following general constraints,
    1. Write expression syntax with in the supported range of javascript features
    2. The compiler can only reference symbols which are exported
    3. Only call the functions supported by the compiler
    4. Decorated and data-bound class members must be public.

  **[⬆ Back to Top](#table-of-contents)**

83. ### What are the three phases of AOT?
    The AOT compiler works in three phases,
    1. **Code Analysis:** The compiler records a representation of the source
    2. **Code generation:** It handles the interpretation as well as places restrictions on what it interprets.
    3. **Validation:** In this phase, the Angular template compiler uses the TypeScript compiler to validate the binding expressions in templates.

  **[⬆ Back to Top](#table-of-contents)**

84. ### Can I use arrow functions in AOT?
    No, Arrow functions or lambda functions can’t be used to assign values to the decorator properties. For example, the following snippet is invalid:

    ```javascript
    @Component({
      providers: [{
        provide: MyService, useFactory: () => getService()
      }]
    })
    ```

    To fix this, it has to be changed as following exported function:

    ```javascript
    function getService(){
      return new MyService();
    }

    @Component({
      providers: [{
        provide: MyService, useFactory: getService
      }]
    })
    ```

    If you still use arrow function, it generates an error node in place of the function. When the compiler later interprets this node, it reports an error to turn the arrow function into an exported function.
    **Note:** From Angular5 onwards, the compiler automatically performs this rewriting while emitting the .js file.

  **[⬆ Back to Top](#table-of-contents)**

85. ### What is the purpose of metadata json files?
    The metadata.json file can be treated as a diagram of the overall structure of a decorator's metadata, represented as an abstract syntax tree(AST). During the analysis phase, the AOT collector scan the metadata recorded in the Angular decorators and outputs metadata information in .metadata.json files, one per .d.ts file.

  **[⬆ Back to Top](#table-of-contents)**

86. ### Can I use any javascript feature for expression syntax in AOT?
    No, the AOT collector understands a subset  of (or limited) JavaScript features. If an expression uses unsupported syntax, the collector writes an error node to the .metadata.json file. Later point of time, the compiler reports an error if it needs that piece of metadata to generate the application code.

  **[⬆ Back to Top](#table-of-contents)**

87. ### What is folding?
    The compiler can only resolve references to exported symbols in the metadata. Where as some of the non-exported members are folded while generating the code. i.e Folding is a process in which the collector evaluate an expression during collection and record the result in the .metadata.json instead of the original expression.
    For example, the compiler couldn't refer selector reference because it is not exported

    ```javascript
    let selector = 'app-root';
    @Component({
      selector: selector
    })
    ```
    Will be folded into inline selector

    ```javascript
    @Component({
          selector: 'app-root'
        })
    ```
    Remember that the compiler can’t fold everything. For example, spread operator on arrays, objects created using new keywords and function calls.

  **[⬆ Back to Top](#table-of-contents)**

88. ### What are macros?
    The AOT compiler supports macros in the form of functions or static methods that return an expression in a `single return expression`.
    For example, let us take a below macro function,

    ```javascript
    export function wrapInArray<T>(value: T): T[] {
      return [value];
    }
    ```

    You can use it inside metadata as an expression,

    ```javascript
    @NgModule({
      declarations: wrapInArray(TypicalComponent)
    })
    export class TypicalModule {}
    ```

    The compiler treats the macro expression as it written directly

    ```javascript
    @NgModule({
      declarations: [TypicalComponent]
    })
    export class TypicalModule {}
    ```

  **[⬆ Back to Top](#table-of-contents)**

89. ### Give an example of few metadata errors?
    Below are some of the errors encountered in metadata,

    1. **Expression form not supported:** Some of the language features outside of the compiler's restricted expression syntax used in angular metadata can produce this error.
        Let's see some of these examples,
        ```javascript
        1. export class User { ... }
           const prop = typeof User; // typeof is not valid in metadata
        2. { provide: 'token', useValue: { [prop]: 'value' } }; // bracket notation is not valid in metadata
        ```
    2. **Reference to a local (non-exported) symbol:** The compiler encountered a referenced to a locally defined symbol that either wasn't exported or wasn't initialized.
        Let's take example of this error,
        ```javascript
        // ERROR
        let username: string; // neither exported nor initialized

        @Component({
          selector: 'my-component',
          template: ... ,
          providers: [
            { provide: User, useValue: username }
          ]
        })
        export class MyComponent {}
        ```
        You can fix this by either exporting or initializing the value,
        ```javascript
        export let username: string; // exported
        (or)
        let username = 'John'; // initialized
        ```
     3. **Function calls are not supported:** The compiler does not currently support function expressions or lambda functions. For example, you cannot set a provider's useFactory to an anonymous function or arrow function as below.
        ```javascript
         providers: [
            { provide: MyStrategy, useFactory: function() { ... } },
            { provide: OtherStrategy, useFactory: () => { ... } }
          ]
        ```
        You can fix this with exported function
        ```javascript
        export function myStrategy() { ... }
        export function otherStrategy() { ... }
        ... // metadata
        providers: [
            { provide: MyStrategy, useFactory: myStrategy },
            { provide: OtherStrategy, useFactory: otherStrategy },
        ```
     4. **Destructured variable or constant not supported:** The compiler does not support references to variables assigned by destructuring.
        For example, you cannot write something like this:
        ```javascript
        import { user } from './user';

        // destructured assignment to name and age
        const {name, age} = user;
        ... //metadata
        providers: [
            {provide: Name, useValue: name},
            {provide: Age, useValue: age},
          ]
        ```
        You can fix this by non-destructured values
        ```javascript
        import { user } from './user';
        ... //metadata
        providers: [
            {provide: Name, useValue: user.name},
            {provide: Age, useValue: user.age},
          ]
        ```

  **[⬆ Back to Top](#table-of-contents)**

90. ### What is metadata rewriting?
    Metadata rewriting is the process in which the compiler converts the expression initializing the fields such as useClass, useValue, useFactory, and data into an exported variable, which replaces the expression. Remember that the compiler does this rewriting during the emit of the .js file but not in definition files( .d.ts file).

  **[⬆ Back to Top](#table-of-contents)**

91. ### How do you provide configuration inheritance?
    Angular Compiler supports configuration inheritance through extends in the tsconfig.json on angularCompilerOptions. i.e, The configuration from the base file(for example, tsconfig.base.json) are loaded first, then overridden by those in the inheriting config file.

    ```javascript
    {
      "extends": "../tsconfig.base.json",
      "compilerOptions": {
        "experimentalDecorators": true,
        ...
      },
      "angularCompilerOptions": {
        "fullTemplateTypeCheck": true,
        "preserveWhitespaces": true,
        ...
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

92. ### How do you specify angular template compiler options?
    The angular template compiler options are specified as members of the **angularCompilerOptions** object in the tsconfig.json file. These options will be specified adjacent to typescript compiler options.

    ```javascript
    {
      "compilerOptions": {
        "experimentalDecorators": true,
                  ...
      },
      "angularCompilerOptions": {
        "fullTemplateTypeCheck": true,
        "preserveWhitespaces": true,
                  ...
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

93. ### How do you enable binding expression validation?
    You can enable binding expression validation explicitly by adding the compiler option **fullTemplateTypeCheck** in the "angularCompilerOptions" of the project's tsconfig.json. It produces error messages when a type error is detected in a template binding expression.

    For example, consider the following component:
    ```javascript
    @Component({
      selector: 'my-component',
      template: '{{user.contacts.email}}'
    })
    class MyComponent {
      user?: User;
    }
    ```
    This will produce the following error:
    ```javascript
    my.component.ts.MyComponent.html(1,1): : Property 'contacts' does not exist on type 'User'. Did you mean 'contact'?
    ```

  **[⬆ Back to Top](#table-of-contents)**

94. ### What is the purpose of any type cast function?
    You can disable binding expression type checking using $any() type cast function(by surrounding the expression). In the following example, the error Property contacts does not exist is suppressed by casting user to the any type.
    ```javascript
      template:
      '{{ $any(user).contacts.email }}'
    ```
    The $any() cast function also works with this to allow access to undeclared members of the component.
    ```javascript
       template:
       '{{ $any(this).contacts.email }}'
    ```

  **[⬆ Back to Top](#table-of-contents)**

95. ### What is Non null type assertion operator?
    You can use the non-null type assertion operator to suppress the Object is possibly 'undefined' error. In the following example, the user and contact properties are always set together, implying that contact is always non-null if user is non-null. The error is suppressed in the example by using contact!.email.
    ```javascript
    @Component({
      selector: 'my-component',
      template: '<span *ngIf="user"> {{user.name}} contacted through {{contact!.email}} </span>'
    })
    class MyComponent {
      user?: User;
      contact?: Contact;

      setData(user: User, contact: Contact) {
        this.user = user;
        this.contact = contact;
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

96. ### What is type narrowing?
    The expression used in an ngIf directive is used to narrow type unions in the Angular template compiler similar to if expression in typescript. So *ngIf allows the typeScript compiler to infer that the data used in the binding expression will never be undefined.
    ```javascript
    @Component({
      selector: 'my-component',
      template: '<span *ngIf="user"> {{user.contact.email}} </span>'
    })
    class MyComponent {
      user?: User;
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

97. ### How do you describe various dependencies in angular application?
    The dependencies section of package.json with in an angular application can be divided as follow,

    1. **Angular packages:** Angular core and optional modules; their package names begin @angular/.
    2. **Support packages:** Third-party libraries that must be present for Angular apps to run.
    3. **Polyfill packages:** Polyfills plug gaps in a browser's JavaScript implementation.

  **[⬆ Back to Top](#table-of-contents)**

99. ### What is the purpose of common module?
    The commonly-needed services, pipes, and directives provided by @angular/common module. Apart from these HttpClientModule is available under @angular/common/http.

  **[⬆ Back to Top](#table-of-contents)**

100. ### What is codelyzer?
     Codelyzer provides set of tslint rules for static code analysis of Angular TypeScript projects. You can run the static code analyzer over web apps, NativeScript, Ionic etc. Angular CLI has support for this and it can be use as below,
     ```bash
     ng new codelyzer
     ng lint
     ```

   **[⬆ Back to Top](#table-of-contents)**

101. ### What is angular animation?
     Angular's animation system is built on CSS functionality in order to animate any property that the browser considers animatable. These properties includes positions, sizes, transforms, colors, borders etc. The Angular modules for animations are **@angular/animations** and **@angular/platform-browser** and these dependencies are automatically added to your project when you create a project using Angular CLI.

   **[⬆ Back to Top](#table-of-contents)**

102. ### What are the steps to use animation module?
     You need to follow below steps to implement animation in your angular project,

     1. **Enabling the animations module:** Import BrowserAnimationsModule to add animation capabilities into your Angular root application module(for example, src/app/app.module.ts).
         ```javascript
         import { NgModule } from '@angular/core';
         import { BrowserModule } from '@angular/platform-browser';
         import { BrowserAnimationsModule } from '@angular/platform-browser/animations';

         @NgModule({
           imports: [
             BrowserModule,
             BrowserAnimationsModule
           ],
           declarations: [ ],
           bootstrap: [ ]
         })
         export class AppModule { }
         ```
     2. **Importing animation functions into component files:** Import required animation functions from @angular/animations in component files(for example, src/app/app.component.ts).
         ```javascript
         import {
           trigger,
           state,
           style,
           animate,
           transition,
           // ...
         } from '@angular/animations';
         ```
     3. **Adding the animation metadata property:** add a metadata property called animations: within the @Component() decorator in component files(for example, src/app/app.component.ts)
         ```javascript
         @Component({
           selector: 'app-root',
           templateUrl: 'app.component.html',
           styleUrls: ['app.component.css'],
           animations: [
             // animation triggers go here
           ]
         })
         ```

   **[⬆ Back to Top](#table-of-contents)**

103. ### What is State function?
     Angular's state() function is used to define different states to call at the end of each transition. This function takes two arguments: a unique name like open or closed and a style() function.

     For example, you can write a open state function

     ```javascript
     state('open', style({
       height: '300px',
       opacity: 0.5,
       backgroundColor: 'blue'
     })),
     ```

   **[⬆ Back to Top](#table-of-contents)**

104. ### What is Style function?
     The style function is used to define a set of styles to associate with a given state name. You need to use it along with state() function to set CSS style attributes. For example, in the close state, the button has a height of 100 pixels, an opacity of 0.8, and a background color of green.

     ```javascript
     state('close', style({
       height: '100px',
       opacity: 0.8,
       backgroundColor: 'green'
     })),
     ```
     **Note:** The style attributes must be in camelCase.

   **[⬆ Back to Top](#table-of-contents)**

105. ### What is the purpose of animate function?
     Angular Animations are a powerful way to implement sophisticated and compelling animations for your Angular single page web application.

        ```javascript
        import { Component, OnInit, Input } from '@angular/core';
        import { trigger, state, style, animate, transition } from '@angular/animations';
    
        @Component({
        selector: 'app-animate',
        templateUrl: `<div [@changeState]="currentState" class="myblock mx-auto"></div>`,
        styleUrls: `.myblock {
            background-color: green;
            width: 300px;
            height: 250px;
            border-radius: 5px;
            margin: 5rem;
            }`,
        animations: [
            trigger('changeState', [
            state('state1', style({
                backgroundColor: 'green',
                transform: 'scale(1)'
            })),
            state('state2', style({
                backgroundColor: 'red',
                transform: 'scale(1.5)'
            })),
            transition('*=>state1', animate('300ms')),
            transition('*=>state2', animate('2000ms'))
            ])
        ]
        })
        export class AnimateComponent implements OnInit {
    
            @Input() currentState;
    
            constructor() { }
    
            ngOnInit() {
            }
        }
        ```

   **[⬆ Back to Top](#table-of-contents)**

106. ### What is transition function?
     The animation transition function is used to specify the changes that occur between one state and another over a period of time. It accepts two arguments: the first argument accepts an expression that defines the direction between two transition states, and the second argument accepts an animate() function.

     Let's take an example state transition from open to closed with an half second transition between states.

     ```javascript
     transition('open => closed', [
       animate('500ms')
     ]),
     ```

   **[⬆ Back to Top](#table-of-contents)**

107. ### How to inject the dynamic script in angular?
     Using DomSanitizer we can inject the dynamic Html,Style,Script,Url.

     ```
     import { Component, OnInit } from '@angular/core';
     import { DomSanitizer } from '@angular/platform-browser';
     @Component({
        selector: 'my-app',
        template: `
            <div [innerHtml]="htmlSnippet"></div>
        `,
     })
     export class App {
            constructor(protected sanitizer: DomSanitizer) {}
            htmlSnippet: string = this.sanitizer.bypassSecurityTrustScript("<script>safeCode()</script>");
        }
     ```

   **[⬆ Back to Top](#table-of-contents)**

 108. ### What is a service worker and its role in Angular?
      A service worker is a script that runs in the web browser and manages caching for an application. Starting from 5.0.0 version, Angular ships with a service worker implementation. Angular service worker is designed to optimize the end user experience of using an application over a slow or unreliable network connection, while also minimizing the risks of serving outdated content.

   **[⬆ Back to Top](#table-of-contents)**

 109. ### What are the design goals of service workers?
      Below are the list of design goals of Angular's service workers,

      1. It caches an application just like installing a native application
      2. A running application continues to run with the same version of all files without any incompatible files
      3. When you refresh the application, it loads the latest fully cached version
      4. When changes are published then it immediately updates in the background
      5. Service workers saves the bandwidth by downloading the resources only when they changed.

   **[⬆ Back to Top](#table-of-contents)**

 110. ### What are the differences between AngularJS and Angular with respect to dependency injection?
      Dependency injection is a common component in both AngularJS and Angular, but there are some key differences between the two frameworks in how it actually works.

        | AngularJS | Angular |
        |---- | ---------
        | Dependency injection tokens are always strings  | Tokens can have different types. They are often classes and sometimes can be strings. |
        | There is exactly one injector even though it is a multi-module applications | There is a tree hierarchy of injectors, with a root injector and an additional injector for each component. |

   **[⬆ Back to Top](#table-of-contents)**

 111. ### What is Angular Ivy?
      Angular Ivy is a new rendering engine for Angular. You can choose to opt in a preview version of Ivy from Angular version 8.

      1. You can enable ivy in a new project by using the --enable-ivy flag with the ng new command

          ```bash
          ng new ivy-demo-app --enable-ivy
          ```
      2. You can add it to an existing project by adding `enableIvy` option in the `angularCompilerOptions` in your project's `tsconfig.app.json`.

          ```javascript
          {
            "compilerOptions": { ... },
            "angularCompilerOptions": {
              "enableIvy": true
            }
          }
          ```

   **[⬆ Back to Top](#table-of-contents)**

 112. ### What are the features included in ivy preview?
      You can expect below features with Ivy preview,

      1. Generated code that is easier to read and debug at runtime
      2. Faster re-build time
      3. Improved payload size
      4. Improved template type checking

   **[⬆ Back to Top](#table-of-contents)**

 113. ### Can I use AOT compilation with Ivy?
      Yes, it is a recommended configuration. Also, AOT compilation with Ivy is faster. So you need set the default build options(with in angular.json) for your project to always use AOT compilation.

      ```javascript
      {
        "projects": {
          "my-project": {
            "architect": {
              "build": {
                "options": {
                  ...
                  "aot": true,
                }
              }
            }
          }
        }
      }
      ```

   **[⬆ Back to Top](#table-of-contents)**

 114. ### What is Angular Language Service?
      The Angular Language Service is a way to get completions, errors, hints, and navigation inside your Angular templates whether they are external in an HTML file or embedded in annotations/decorators in a string. It has the ability to autodetect that you are opening an Angular file, reads your `tsconfig.json` file, finds all the templates you have in your application, and then provides all the language services.

   **[⬆ Back to Top](#table-of-contents)**

 115. ### How do you install angular language service in the project?
      You can install Angular Language Service in your project with the following npm command,

      ```javascript
      npm install --save-dev @angular/language-service
      ```
      After that add the following to the "compilerOptions" section of your project's tsconfig.json

      ```javascript
      "plugins": [
          {"name": "@angular/language-service"}
      ]
      ```
      **Note:** The completion and diagnostic services works for .ts files only. You need to use custom plugins for supporting HTML files.

   **[⬆ Back to Top](#table-of-contents)**

 116. ### Is there any editor support for Angular Language Service?
      Yes, Angular Language Service is currently available for Visual Studio Code and WebStorm IDEs. You need to install angular language service using an extension and devDependency respectively. In sublime editor, you need to install typescript which has has a language service plugin model.

   **[⬆ Back to Top](#table-of-contents)**

 117. ### Explain the features provided by Angular Language Service?
      Basically there are 3 main features provided by Angular Language Service,

      1. **Autocompletion:** Autocompletion can speed up your development time by providing you with contextual possibilities and hints as you type with in an interpolation and elements.

           ![ScreenShot](images/language-completion.gif)

      2. **Error checking:** It can also warn you of mistakes in your code.

           ![ScreenShot](images/language-error.gif)

      3. **Navigation:** Navigation allows you to hover a component, directive, module and then click and press F12 to go directly to its definition.

           ![ScreenShot](images/language-navigation.gif)

   **[⬆ Back to Top](#table-of-contents)**

 118. ### How do you add web workers in your application?
      You can add web worker anywhere in your application. For example, If the file that contains your expensive computation is `src/app/app.component.ts`, you can add a Web Worker using `ng generate web-worker app` command which will create `src/app/app.worker.ts` web worker file. This command will perform below actions,

      1. Configure your project to use Web Workers
      2. Adds app.worker.ts to receive messages
          ```javascript
          addEventListener('message', ({ data }) => {
            const response = `worker response to ${data}`;
            postMessage(response);
          });
          ```
      3. The component `app.component.ts` file updated with web worker file
          ```javascript
          if (typeof Worker !== 'undefined') {
            // Create a new
            const worker = new Worker('./app.worker', { type: 'module' });
            worker.onmessage = ({ data }) => {
              console.log('page got message: $\{data\}');
            };
            worker.postMessage('hello');
          } else {
            // Web Workers are not supported in this environment.
          }
          ```

      **Note:** You may need to refactor your initial scaffolding web worker code for sending messages to and from.

   **[⬆ Back to Top](#table-of-contents)**

 119. ### What are the limitations with web workers?
      You need to remember two important things when using Web Workers in Angular projects,

      1. Some environments or platforms(like @angular/platform-server) used in Server-side Rendering, don't support Web Workers. In this case you need to provide a fallback mechanism to perform the computations to work in this environments.
      2. Running Angular in web worker using `@angular/platform-webworker` is not yet supported in Angular CLI.

   **[⬆ Back to Top](#table-of-contents)**

 121. ### What is a builder?
      A builder function is a function that uses the `Architect API` to perform a complex process such as "build" or "test". The builder code is defined in an npm package. For example, BrowserBuilder runs a webpack build for a browser target and KarmaBuilder starts the Karma server and runs a webpack build for unit tests.

   **[⬆ Back to Top](#table-of-contents)**

 122. ### How do you invoke a builder?
      The Angular CLI command `ng run` is used to invoke a builder with a specific target configuration. The workspace configuration file, `angular.json`, contains default configurations for built-in builders.

   **[⬆ Back to Top](#table-of-contents)**

 123. ### How do you create app shell in Angular?
      An App shell is a way to render a portion of your application via a route at build time. This is useful to first paint of your application that appears quickly because the browser can render static HTML and CSS without the need to initialize JavaScript. You can achieve this using Angular CLI which generates an app shell for running server-side of your app.

      ```javascript
      ng generate appShell [options] (or)
      ng g appShell [options]
      ```

   **[⬆ Back to Top](#table-of-contents)**

 124. ### What are the case types in Angular?
      Angular uses capitalization conventions to distinguish the names of various types. Angular follows the list of the below case types.

      1. **camelCase :** Symbols, properties, methods, pipe names, non-component directive selectors, constants uses lowercase on the first letter of the item. For example, "selectedUser"
      2. **UpperCamelCase (or PascalCase):** Class names, including classes that define components, interfaces, NgModules, directives, and pipes uses uppercase on the first letter of the item.
      3. **dash-case (or "kebab-case"):** The descriptive part of file names, component selectors uses dashes between the words. For example, "app-user-list".
      4. **UPPER_UNDERSCORE_CASE:** All constants uses capital letters connected with underscores. For example, "NUMBER_OF_USERS".

   **[⬆ Back to Top](#table-of-contents)**

 125. ### What are the class decorators in Angular?
      A class decorator is a decorator that appears immediately before a class definition, which declares the class to be of the given type, and provides metadata suitable to the type

      The following list of decorators comes under class decorators,

      1. @Component()
      2. @Directive()
      3. @Pipe()
      4. @Injectable()
      5. @NgModule()

   **[⬆ Back to Top](#table-of-contents)**

 126. ### What are class field decorators?
      The class field decorators are the statements declared immediately before a field in a class definition that defines the type of that field. Some of the examples are: @input and @output,

      ```javascript
      @Input() myProperty;
      @Output() myEvent = new EventEmitter();
      ```

   **[⬆ Back to Top](#table-of-contents)**

 127. ### What is declarable in Angular?
      Declarable is a class type that you can add to the declarations list of an NgModule. The class types such as components, directives, and pipes comes can be declared in the module. The structure of declarations would be,

      ```javascript
      declarations: [
        YourComponent,
        YourPipe,
        YourDirective
      ],
      ```

   **[⬆ Back to Top](#table-of-contents)**

 128. ### What are the restrictions on declarable classes?
      Below classes shouldn't be declared,

      1. A class that's already declared in another NgModule
      2. Ngmodule classes
      3. Service classes
      4. Helper classes

   **[⬆ Back to Top](#table-of-contents)**

 129. ### What is a DI token?
      A DI token is a lookup token associated with a dependency provider in dependency injection system. The injector maintains an internal token-provider map that it references when asked for a dependency and the DI token is the key to the map. Let's take example of DI Token usage,

      ```javascript
      const BASE_URL = new InjectionToken<string>('BaseUrl');
      const injector =
         Injector.create({providers: [{provide: BASE_URL, useValue: 'http://some-domain.com'}]});
      const url = injector.get(BASE_URL);
      ```

   **[⬆ Back to Top](#table-of-contents)**

 130. ### What is Angular DSL?
      A domain-specific language (DSL) is a computer language specialized to a particular application domain. Angular has its own Domain Specific Language (DSL) which allows us to write Angular specific html-like syntax on top of normal html. It has its own compiler that compiles this syntax to html that the browser can understand. This DSL is defined in NgModules such as animations, forms, and routing and navigation.

      Basically you will see 3 main syntax in Angular DSL.

      1. `()`: Used for Output and DOM events.
      2. `[]`: Used for Input and specific DOM element attributes.
      3. `*`: Structural directives(*ngFor or *ngIf) will affect/change the DOM structure.

   **[⬆ Back to Top](#table-of-contents)**

131. ### what is an rxjs subject in Angular
     An RxJS Subject is a special type of Observable that allows values to be multicasted to many Observers. While plain Observables are unicast (each subscribed Observer owns an independent execution of the Observable), Subjects are multicast.
      
     A Subject is like an Observable, but can multicast to many Observers. Subjects are like EventEmitters: they maintain a registry of many listeners.

     ``` typescript
      import { Subject } from 'rxjs';
 
        const subject = new Subject<number>();

        subject.subscribe({
          next: (v) => console.log(`observerA: ${v}`)
        });
        subject.subscribe({
          next: (v) => console.log(`observerB: ${v}`)
        });

        subject.next(1);
        subject.next(2);
     ```

   **[⬆ Back to Top](#table-of-contents)**

132.  ### What is Bazel tool?
      Bazel is a powerful build tool developed and massively used by Google and it can keep track of the dependencies between different packages and build targets. In Angular8, you can build your CLI application with Bazel.
      **Note:** The Angular framework itself is built with Bazel.

   **[⬆ Back to Top](#table-of-contents)**

133.  ### What are the advantages of Bazel tool?
      Below are the list of key advantages of Bazel tool,

      1. It creates the possibility of building your back-ends and front-ends with the same tool
      2. The incremental build and tests
      3. It creates the possibility to have remote builds and cache on a build farm.

   **[⬆ Back to Top](#table-of-contents)**

134. ### How do you use Bazel with Angular CLI?
     The @angular/bazel package provides a builder that allows Angular CLI to use Bazel as the build tool.
     1. **Use in an existing application:** Add @angular/bazel using CLI
         ```javascript
         ng add @angular/bazel
         ```
     2. **Use in a new application:** Install the package and create the application with collection option
         ```javascript
         npm install -g @angular/bazel
         ng new --collection=@angular/bazel
         ```
     When you use ng build and ng serve commands, Bazel is used behind the scenes and outputs the results in dist/bin folder.

   **[⬆ Back to Top](#table-of-contents)**

135. ### How do you run Bazel directly?
     Sometimes you may want to bypass the Angular CLI builder and run Bazel directly using Bazel CLI. You can install it globally using @bazel/bazel npm package. i.e, Bazel CLI is available under @bazel/bazel package. After you can apply the below common commands,

     ```javascrippt
     bazel build [targets] // Compile the default output artifacts of the given targets.
     bazel test [targets] // Run the tests with *_test targets found in the pattern.
     bazel run [target]: Compile the program represented by target and then run it.
     ```

   **[⬆ Back to Top](#table-of-contents)**

136. ### What is platform in Angular?
     A platform is the context in which an Angular application runs. The most common platform for Angular applications is a web browser, but it can also be an operating system for a mobile device, or a web server. The runtime-platform is provided by the @angular/platform-* packages and these packages allow applications that make use of `@angular/core` and `@angular/common` to execute in different environments.
     i.e, Angular can be used as platform-independent framework in different environments, For example,

     1. While running in the browser, it uses `platform-browser` package.
     2. When SSR(server-side rendering ) is used, it uses `platform-server` package for providing web server implementation.

   **[⬆ Back to Top](#table-of-contents)**

137. ### What happens if I import the same module twice?
     If multiple modules imports the same module then angular evaluates it only once (When it encounters the module first time). It follows this condition even the module appears at any level in a hierarchy of imported NgModules.

   **[⬆ Back to Top](#table-of-contents)**

138. ### How do you select an element with in a component template?
     You can use `@ViewChild` directive to access elements in the view directly. Let's take input element with a reference,

     ```html
     <input #uname>
     ```
     and define view child directive and access it in ngAfterViewInit lifecycle hook

     ```javascript
     @ViewChild('uname') input;

     ngAfterViewInit() {
       console.log(this.input.nativeElement.value);
     }
     ```

   **[⬆ Back to Top](#table-of-contents)**

139. ### How do you detect route change in Angular?
     In Angular7, you can subscribe to router to detect the changes. The subscription for router events would be as below,

     ```javascript
     this.router.events.subscribe((event: Event) => {})
     ```
     Let's take a simple component to detect router changes

     ```javascript
     import { Component } from '@angular/core';
     import { Router, Event, NavigationStart, NavigationEnd, NavigationError } from '@angular/router';

     @Component({
         selector: 'app-root',
         template: `<router-outlet></router-outlet>`
     })
     export class AppComponent {

         constructor(private router: Router) {

             this.router.events.subscribe((event: Event) => {
                 if (event instanceof NavigationStart) {
                     // Show loading indicator and perform an action
                 }

                 if (event instanceof NavigationEnd) {
                     // Hide loading indicator and perform an action
                 }

                 if (event instanceof NavigationError) {
                     // Hide loading indicator and perform an action
                     console.log(event.error); // It logs an error for debugging
                 }
             });
        }
     }
     ```

   **[⬆ Back to Top](#table-of-contents)**

140. ### How do you pass headers for HTTP client?
     You can directly pass object map for http client or create HttpHeaders class to supply the headers.

     ```javascript
     constructor(private _http: HttpClient) {}
     this._http.get('someUrl',{
        headers: {'header1':'value1','header2':'value2'}
     });

     (or)
     let headers = new HttpHeaders().set('header1', headerValue1); // create header object
     headers = headers.append('header2', headerValue2); // add a new header, creating a new object
     headers = headers.append('header3', headerValue3); // add another header

     let params = new HttpParams().set('param1', value1); // create params object
     params = params.append('param2', value2); // add a new param, creating a new object
     params = params.append('param3', value3); // add another param

     return this._http.get<any[]>('someUrl', { headers: headers, params: params })
     ```

     **[⬆ Back to Top](#table-of-contents)**

141. ### What is the purpose of differential loading in CLI?
     From Angular8 release onwards, the applications are built using differential loading strategy from CLI to build two separate bundles as part of your deployed application.

     1. The first build contains ES2015 syntax which takes the advantage of built-in support in modern browsers, ships less polyfills, and results in a smaller bundle size.
     2. The second build contains old ES5 syntax to support older browsers with all necessary polyfills. But this results in a larger bundle size.

     **Note:** This strategy is used to support multiple browsers but it only load the code that the browser needs.

     **[⬆ Back to Top](#table-of-contents)**

142. ### Is Angular supports dynamic imports?
     Yes, Angular 8 supports dynamic imports in router configuration. i.e, You can use the import statement for lazy loading the module using `loadChildren` method and it will be understood by the IDEs(VSCode and WebStorm), webpack, etc.
     Previously, you have been written as below to lazily load the feature module. By mistake, if you have typo in the module name it still accepts the string and throws an error during build time.
     ```javascript
     {path: ‘user’, loadChildren: ‘./users/user.module#UserModulee’},
     ```
     This problem is resolved by using dynamic imports and IDEs are able to find it during compile time itself.
     ```javascript
     {path: ‘user’, loadChildren: () => import(‘./users/user.module’).then(m => m.UserModule)};
     ```

     **[⬆ Back to Top](#table-of-contents)**

144. ### What are workspace APIs?
     Angular 8.0 release introduces Workspace APIs to make it easier for developers to read and modify the angular.json file instead of manually modifying it. Currently, the only supported storage3 format is the JSON-based format used by the Angular CLI. You can enable or add optimization option for build target as below,
     ```javascript
     import { NodeJsSyncHost } from '@angular-devkit/core/node';
     import { workspaces } from '@angular-devkit/core';

     async function addBuildTargetOption() {
         const host = workspaces.createWorkspaceHost(new NodeJsSyncHost());
         const workspace = await workspaces.readWorkspace('path/to/workspace/directory/', host);

         const project = workspace.projects.get('my-app');
         if (!project) {
           throw new Error('my-app does not exist');
         }

         const buildTarget = project.targets.get('build');
         if (!buildTarget) {
           throw new Error('build target does not exist');
         }

         buildTarget.options.optimization = true;

         await workspaces.writeWorkspace(workspace, host);
     }

     addBuildTargetOption();
     ```

     **[⬆ Back to Top](#table-of-contents)**

145. ### How do you upgrade angular version?
     The Angular upgrade is quite easier using Angular CLI `ng update` command as mentioned below. For example, if you upgrade from Angular 7 to 8 then your lazy loaded route imports will be migrated to the new import syntax automatically.
     ```bash
     $ ng update @angular/cli @angular/core
     ```

     **[⬆ Back to Top](#table-of-contents)**

146. ### What is Angular Material?
     Angular Material is a collection of Material Design components for Angular framework following the Material Design spec. You can apply Material Design very easily using Angular Material. The installation can be done through npm or yarn,
     ```bash
     npm install --save @angular/material @angular/cdk @angular/animations
     (OR)
     yarn add @angular/material @angular/cdk @angular/animations
     ```
     It supports the most recent two versions of all major browsers. The latest version of Angular material is 8.1.1

     **[⬆ Back to Top](#table-of-contents)**

147. ### How do you upgrade location service of angularjs?
     If you are using `$location` service in your old AngularJS application, now you can use `LocationUpgradeModule`(unified location service) which puts the responsibilities of `$location` service to `Location` service in Angular. Let's add this module to `AppModule` as below,
     ```javascript
     // Other imports ...
     import { LocationUpgradeModule } from '@angular/common/upgrade';

     @NgModule({
       imports: [
         // Other NgModule imports...
         LocationUpgradeModule.config()
       ]
     })
     export class AppModule {}
     ```

     **[⬆ Back to Top](#table-of-contents)**

148. ### What is NgUpgrade?
     NgUpgrade is a library put together by the Angular team, which you can use in your applications to mix and match AngularJS and Angular components and bridge the AngularJS and Angular dependency injection systems.

     **[⬆ Back to Top](#table-of-contents)**

149. ### How do you test Angular application using CLI?
     Angular CLI downloads and install everything needed with the Jasmine Test framework. You just need to run `ng test` to see the test results. By default this command builds the app in watch mode, and launches the `Karma test runner`. The output of test results would be as below,
     ```bash
     10% building modules 1/1 modules 0 active
     ...INFO [karma]: Karma v1.7.1 server started at http://0.0.0.0:9876/
     ...INFO [launcher]: Launching browser Chrome ...
     ...INFO [launcher]: Starting browser Chrome
     ...INFO [Chrome ...]: Connected on socket ...
     Chrome ...: Executed 3 of 3 SUCCESS (0.135 secs / 0.205 secs)
     ```
     **Note:** A chrome browser also opens and displays the test output in the "Jasmine HTML Reporter".

     **[⬆ Back to Top](#table-of-contents)**


150. ### How to use polyfills in Angular application?
     The Angular CLI provides support for polyfills officially. When you create a new project with the ng new command, a `src/polyfills.ts` configuration file is created as part of your project folder. This file includes the mandatory and many of the optional polyfills as JavaScript import statements. Let's categorize the polyfills,

     1. **Mandatory polyfills:** These are installed automatically when you create your project with ng new command and the respective import statements enabled in 'src/polyfills.ts' file.
     2. **Optional polyfills:** You need to install its npm package and then create import statement in 'src/polyfills.ts' file.
        For example, first you need to install below npm package for adding web animations (optional) polyfill.
            ```bash
             npm install --save web-animations-js
            ```
        and create import statement in polyfill file.
            ```javascript
            import 'web-animations-js';
            ```

     **[⬆ Back to Top](#table-of-contents)**

151. ### What are the ways to trigger change detection in Angular?
     You can inject either ApplicationRef or NgZone, or ChangeDetectorRef into your component and apply below specific methods to trigger change detection in Angular. i.e, There are 3 possible ways,

     1. **ApplicationRef.tick():** Invoke this method to explicitly process change detection and its side-effects. It check the full component tree.
     2. **NgZone.run(callback):** It evaluate the callback function inside the Angular zone.
     3. **ChangeDetectorRef.detectChanges():** It detects only the components and it's children.

     **[⬆ Back to Top](#table-of-contents)**

152. ### What are the differences of various versions of Angular?
     There are different versions of Angular framework. Let's see the features of all the various versions,

     1. **Angular 1:**
        * Angular 1 (AngularJS) is the first angular framework released in the year 2010.
        * AngularJS is not built for mobile devices.
        * It is based on controllers with MVC architecture.
     2. **Angular 2:**
        * Angular 2 was released in the year 2016. Angular 2 is a complete rewrite of Angular1 version.
        * The performance issues that Angular 1 version had has been addressed in Angular 2 version.
        * Angular 2 is built from scratch for mobile devices unlike Angular 1 version.
        * Angular 2 is components based.
     3. **Angular 3:**
        * The following are the different package versions in Angular 2:
          * @angular/core v2.3.0
          * @angular/compiler v2.3.0
          * @angular/http v2.3.0
          * @angular/router v3.3.0
        * The router package is already versioned 3 so to avoid confusion switched to Angular 4 version and skipped 3 version.
     4. **Angular 4:**
        * The compiler generated code file size in AOT mode is very much reduced.
        * With Angular 4 the production bundles size is reduced by hundreds of KB’s.
        * Animation features are removed from angular/core and formed as a separate package.
        * Supports Typescript 2.1 and 2.2.
        * Angular Universal
        * New HttpClient
     5. **Angular 5:**
        * Angular 5 makes angular faster. It improved the loading time and execution time.
        * Shipped with new build optimizer.
        * Supports Typescript 2.5.
        * Service Worker
     6. **Angular 6:**
        * It is released in May 2018.
        * Includes Angular Command Line Interface (CLI), Component Development KIT (CDK), Angular Material Package, Angular Elements.
        * Service Worker bug fixes.
        * i18n
        * Experimental mode for Ivy.
        * RxJS 6.0
        * Tree Shaking
     7. **Angular 7:**
        * It is released in October 2018.
        * TypeScript 3.1
        * RxJS 6.3
        * New Angular CLI
        * CLI Prompts capability provide an ability to ask questions to the user before they run. It is like interactive dialog between the user and the CLI
        * With the improved CLI Prompts capability, it helps developers to make the decision. New ng commands ask users for routing and CSS styles types(SCSS) and ng add @angular/material asks for themes and gestures or animations.
      8. **Angular 8:**
         * It is released in May 2019.
         * TypeScript 3.4
      9. **Angular 9:**
         * It is released in February 2020.
         * TypeScript 3.7
         * Ivy enabled by default
      10. **Angular 10:**
            * It is released in June 2020.
            * TypeScript 3.9 
            * TSlib 2.0

      **[⬆ Back to Top](#table-of-contents)**

153. ### What are the security principles in angular?
     Below are the list of security principles in angular,

		1.	You should avoid direct use of the DOM APIs.
		2.  You should enable Content Security Policy (CSP) and configure your web server to return appropriate CSP HTTP headers.
		3.  You should Use the offline template compiler.
		4.  You should Use Server Side XSS protection.
		5.  You should Use DOM Sanitizer.
		6.  You should Preventing CSRF or XSRF attacks. 

	 **[⬆ Back to Top](#table-of-contents)**

154. ### What is the reason to deprecate Web Tracing Framework?
     Angular has supported the integration with the Web Tracing Framework (WTF) for the purpose of performance testing. Since it is not well maintained and failed in majority of the applications, the support is deprecated in latest releases.

     **[⬆ Back to Top](#table-of-contents)**

155. ### What is the reason to deprecate web worker packages?
     Both `@angular/platform-webworker` and `@angular/platform-webworker-dynamic` are officially deprecated, the Angular team realized it's not good practice to run the Angular application on Web worker

     **[⬆ Back to Top](#table-of-contents)**

156. ### How do you find angular CLI version?
     Angular CLI provides it's installed version using below different ways using ng command,

     ```bash
     ng v
     ng version
     ng -v
     ng --version
     ```
     and the output would be as below,

     ```bash
     Angular CLI: 1.6.3
     Node: 8.11.3
     OS: darwin x64
     Angular:
     ...
     ```

     **[⬆ Back to Top](#table-of-contents)**

157. ### What is the browser support for Angular?
     Angular supports most recent browsers which includes both desktop and mobile browsers.

     | Browser | Version |
     |---- | --------- |
     | Chrome | latest |
     | Firefox | latest |
     | Edge | 2 most recent major versions |
     | IE | 11, 10, 9 (Compatibility mode is not supported) |
     | Safari | 2 most recent major versions |
     | IE Mobile | 11 |
     | iOS | 2 most recent major versions |
     | Android | 7.0, 6.0, 5.0, 5.1, 4.4 |

     **[⬆ Back to Top](#table-of-contents)**

158. ### What is schematic?
     It's a scaffolding library that defines how to generate or transform a programming project by creating, modifying, refactoring, or moving files and code. It defines rules that operate on a virtual file system called a tree.

     **[⬆ Back to Top](#table-of-contents)**

159. ### What is rule in Schematics?

     In schematics world, it's a function that operates on a file tree to create, delete, or modify files in a specific manner.

     **[⬆ Back to Top](#table-of-contents)**

160. ### What is Schematics CLI?
     Schematics come with their own command-line tool known as Schematics CLI. It is used to install the schematics executable, which you can use to create a new schematics collection with an initial named schematic. The collection folder is a workspace for schematics. You can also use the schematics command to add a new schematic to an existing collection, or extend an existing schematic. You can install Schematic CLI globally as below,
     ```bash
     npm install -g @angular-devkit/schematics-cli
     ```

     **[⬆ Back to Top](#table-of-contents)**

161. ### What are the best practices for security in angular?
     Below are the best practices of security in angular,

     1. Use the latest Angular library releases
     2. Don't modify your copy of Angular
     3. Avoid Angular APIs marked in the documentation as “Security Risk.”

     **[⬆ Back to Top](#table-of-contents)**

162. ### What is Angular security model for preventing XSS attacks?
     Angular treats all values as untrusted by default. i.e, Angular sanitizes and escapes untrusted values When a value is inserted into the DOM from a template, via property, attribute, style, class binding, or interpolation.

     **[⬆ Back to Top](#table-of-contents)**

163. ### What is the role of template compiler for prevention of XSS attacks?
     The offline template compiler prevents vulnerabilities caused by template injection, and greatly improves application performance. So it is recommended to use offline template compiler in production deployments without dynamically generating any template.

     **[⬆ Back to Top](#table-of-contents)**

164. ### What are the various security contexts in Angular?
     Angular defines the following security contexts for sanitization,

     1. **HTML:** It is used when interpreting a value as HTML such as binding to innerHtml.
     2. **Style:** It is used when binding CSS into the style property.
     3. **URL:** It is used for URL properties such as `<a href>`.
     4. **Resource URL:** It is a URL that will be loaded and executed as code such as `<script src>`.

     **[⬆ Back to Top](#table-of-contents)**

165. ### What is Sanitization? Is angular supports it?
     **Sanitization** is the inspection of an untrusted value, turning it into a value that's safe to insert into the DOM. Yes, Angular supports sanitization. It sanitizes untrusted values for HTML, styles, and URLs but sanitizing resource URLs isn't possible because they contain arbitrary code.

     **[⬆ Back to Top](#table-of-contents)**

166. ### What is the purpose of innerHTML?
     The innerHtml is a property of HTML-Elements, which allows you to set it's html-content programmatically. Let's display the below html code snippet in a `<div>` tag as below using innerHTML binding,

     ```html
     <div [innerHTML]="htmlSnippet"></div>
     ```
     and define the htmlSnippet property from any component
     ```javascript
     export class myComponent {
       htmlSnippet: string = '<b>Hello World</b>, Angular';
     }
     ```
     Unfortunately this property could cause Cross Site Scripting (XSS) security bugs when improperly handled.

     **[⬆ Back to Top](#table-of-contents)**

167. ### What is the difference between interpolated content and innerHTML?
     The main difference between interpolated and innerHTML code is the behavior of code interpreted. Interpolated content is always escaped i.e,  HTML isn't interpreted and the browser displays angle brackets in the element's text content. Where as in innerHTML binding, the content is interpreted i.e, the browser will convert < and > characters as HTMLEntities. For example, the usage in template would be as below,

     ```html
     <p>Interpolated value:</p>
     <div >{{htmlSnippet}}</div>
     <p>Binding of innerHTML:</p>
     <div [innerHTML]="htmlSnippet"></div>
     ```
     and the property defined in a component.

     ```javascript
     export class InnerHtmlBindingComponent {
       htmlSnippet = 'Template <script>alert("XSS Attack")</script> <b>Code attached</b>';
     }
     ```
     Even though innerHTML binding create a chance of XSS attack, Angular recognizes the value as unsafe and automatically sanitizes it.

     **[⬆ Back to Top](#table-of-contents)**

168. ### How do you prevent automatic sanitization?
     Sometimes the applications genuinely need to include executable code such as displaying `<iframe>` from an URL. In this case, you need to prevent automatic sanitization in Angular by saying that you inspected a value, checked how it was generated, and made sure it will always be secure. Basically it involves 2 steps,

     1. Inject DomSanitizer: You can inject DomSanitizer in component as parameter in constructor
     2. Mark the trusted value by calling some of the below methods

         1. bypassSecurityTrustHtml
         2. bypassSecurityTrustScript
         3. bypassSecurityTrustStyle
         4. bypassSecurityTrustUrl
         5. bypassSecurityTrustResourceUrl

     For example,The  usage of dangerous url to trusted url would be as below,

     ```javascript
     constructor(private sanitizer: DomSanitizer) {
       this.dangerousUrl = 'javascript:alert("XSS attack")';
       this.trustedUrl = sanitizer.bypassSecurityTrustUrl(this.dangerousUrl);
     ```

     **[⬆ Back to Top](#table-of-contents)**

169. ### Is safe to use direct DOM API methods in terms of security?
     No,the built-in browser DOM APIs or methods don't automatically protect you from security vulnerabilities. In this case it is recommended to use Angular templates instead of directly interacting with DOM. If it is unavoidable then use the built-in Angular sanitization functions.

     **[⬆ Back to Top](#table-of-contents)**

170. ### What is DOM sanitizer?
     `DomSanitizer` is used to help preventing Cross Site Scripting Security bugs (XSS) by sanitizing values to be safe to use in the different DOM contexts.

     **[⬆ Back to Top](#table-of-contents)**

171. ### How do you support server side XSS protection in Angular application?
     The server-side XSS protection is supported in an angular application by using a templating language that automatically escapes values to prevent XSS vulnerabilities on the server. But don't use a templating language to generate Angular templates on the server side which creates a high risk of introducing template-injection vulnerabilities.

     **[⬆ Back to Top](#table-of-contents)**

172. ### Is angular prevents http level vulnerabilities?
     Angular has built-in support for preventing http level vulnerabilities such as as cross-site request forgery (CSRF or XSRF) and cross-site script inclusion (XSSI). Even though these vulnerabilities need to be mitigated on server-side, Angular provides helpers to make the integration easier on the client side.
     1. HttpClient supports a token mechanism used to prevent XSRF attacks
     2. HttpClient library recognizes the convention of prefixed JSON responses(which non-executable js code with ")]}',\\n" characters) and automatically strips the string ")]}',\\n" from all responses before further parsing

     **[⬆ Back to Top](#table-of-contents)**

174. ### What are the applications of HTTP interceptors?
     The HTTP Interceptors can be used for different variety of tasks,

     1. Authentication
     2. Logging
     3. Caching
     4. Fake backend
     5. URL transformation
     6. Modifying headers

     **[⬆ Back to Top](#table-of-contents)**

175. ### Is multiple interceptors supported in Angular?
     Yes, Angular supports multiple interceptors at a time. You could define multiple interceptors in providers property:
     ```javascript
     providers: [
       { provide: HTTP_INTERCEPTORS, useClass: MyFirstInterceptor, multi: true },
       { provide: HTTP_INTERCEPTORS, useClass: MySecondInterceptor, multi: true }
     ],
     ```
     The interceptors will be called in the order in which they were provided. i.e, MyFirstInterceptor will be called first in the above interceptors configuration.

     **[⬆ Back to Top](#table-of-contents)**

176. ### How can I use interceptor for an entire application?
     You can use same instance of `HttpInterceptors` for the entire app by importing the `HttpClientModule` only in your AppModule, and add the interceptors to the root application injector.
     For example, let's define a class that is injectable in root application.
      ```javascript
      @Injectable()
      export class MyInterceptor implements HttpInterceptor {
        intercept(
          req: HttpRequest<any>,
          next: HttpHandler
        ): Observable<HttpEvent<any>> {

          return next.handle(req).do(event => {
            if (event instanceof HttpResponse) {
                 // Code goes here
            }
          });

        }
      }
      ```
     After that import HttpClientModule in AppModule
     ```javascript
     @NgModule({
       declarations: [AppComponent],
       imports: [BrowserModule, HttpClientModule],
       providers: [
         { provide: HTTP_INTERCEPTORS, useClass: MyInterceptor, multi: true }
       ],
       bootstrap: [AppComponent]
     })
     export class AppModule {}
     ```

     **[⬆ Back to Top](#table-of-contents)**

177. ### How does Angular simplifies Internationalization?

     Angular simplifies the below areas of internationalization,
     1. Displaying dates, number, percentages, and currencies in a local format.
     2. Preparing text in component templates for translation.
     3. Handling plural forms of words.
     4. Handling alternative text.

     **[⬆ Back to Top](#table-of-contents)**

178. ### How do you manually register locale data?
     By default, Angular only contains locale data for en-US which is English as spoken in the United States of America . But if you want to set to another locale, you must import locale data for that new locale. After that you can register using `registerLocaleData` method and the syntax of this method looks like below,
     ```javascript
     registerLocaleData(data: any, localeId?: any, extraData?: any): void
     ```
     For example, let us import German locale and register it in the application
     ```javascript
     import { registerLocaleData } from '@angular/common';
     import localeDe from '@angular/common/locales/de';

     registerLocaleData(localeDe, 'de');
     ```

     **[⬆ Back to Top](#table-of-contents)**

179. ### What are the four phases of template translation?
     The i18n template translation process has four phases:

     1. **Mark static text messages in your component templates for translation:** You can place i18n on every element tag whose fixed text is to be translated. For example, you need i18n attribute for heading as below,
         ```javascript
         <h1 i18n>Hello i18n!</h1>
         ```

     2. **Create a translation file:** Use the Angular CLI xi18n command to extract the marked text into an industry-standard translation source file. i.e, Open terminal window at the root of the app project and run the CLI command xi18n.
         ```bash
         ng xi18n
         ```
        The above command creates a file named `messages.xlf` in your project's root directory.

        **Note:** You can supply command options to change the format, the name, the location, and the source locale of the extracted file.

     3. **Edit the generated translation file:** Translate the extracted text into the target language. In this step, create a localization folder (such as `locale`)under root directory(src) and then create target language translation file by copying and renaming the default messages.xlf file. You need to copy source text node and provide the translation under target tag.
         For example, create the translation file(messages.de.xlf) for German language
         ```javascript
         <trans-unit id="greetingHeader" datatype="html">
           <source>Hello i18n!</source>
           <target>Hallo i18n !</target>
           <note priority="1" from="description">A welcome header for this sample</note>
           <note priority="1" from="meaning">welcome message</note>
         </trans-unit>
         ```

     4. **Merge the completed translation file into the app:** You need to use Angular CLI build command to compile the app, choosing a locale-specific configuration, or specifying the following command options.

           1. --i18nFile=path to the translation file
           2. --i18nFormat=format of the translation file
           3. --i18nLocale= locale id

     **[⬆ Back to Top](#table-of-contents)**

180. ### What is the purpose of i18n attribute?
     The Angular i18n attribute marks translatable content. It is a custom attribute, recognized by Angular tools and compilers. The compiler removes it after translation.

     **Note:** Remember that i18n is not an Angular directive.

     **[⬆ Back to Top](#table-of-contents)**

181. ### What is the purpose of custom id?
     When you change the translatable text, the Angular extractor tool generates a new id for that translation unit. Because of this behavior, you must then update the translation file with the new id every time.

     For example, the translation file `messages.de.xlf.html` has generated trans-unit for some text message as below
     ```html
     <trans-unit id="827wwe104d3d69bf669f823jjde888" datatype="html">
     ```
     You can avoid this manual update of `id` attribute by specifying a custom id in the i18n attribute by using the prefix @@.
     ```javascript
     <h1 i18n="@@welcomeHeader">Hello i18n!</h1>
     ```

     **[⬆ Back to Top](#table-of-contents)**

182. ### What happens if the custom id is not unique?
     You need to define custom ids as unique. If you use the same id for two different text messages then only the first one is extracted. But its translation is used in place of both original text messages.

     For example, let's define same custom id `myCustomId` for two messages,
     ```html
     <h2 i18n="@@myCustomId">Good morning</h3>
     <!-- ... -->
     <h2 i18n="@@myCustomId">Good night</p>
     ```
     and the translation unit generated for first text in for German language as
     ```html
     <trans-unit id="myId" datatype="html">
       <source>Good morning</source>
       <target state="new">Guten Morgen</target>
     </trans-unit>
     ```
     Since custom id is the same, both of the elements in the translation contain the same text as below
     ```html
     <h2>Guten Morgen</h2>
     <h2>Guten Morgen</h2>
     ```

     **[⬆ Back to Top](#table-of-contents)**

183. ### Can I translate text without creating an element?
     Yes, you can achieve using `<ng-container>` attribute. Normally you need to wrap a text content with i18n attribute for the translation. But if you don't want to create a new DOM element just for the sake of translation, you can wrap the text in an <ng-container> element.
     ```html
     <ng-container i18n>I'm not using any DOM element for translation</ng-container>
     ```
     Remember that `<ng-container>` is transformed into an html comment

     **[⬆ Back to Top](#table-of-contents)**

184. ### How can I translate attribute?
     You can translate attributes by attaching `i18n-x` attribute  where x is the name of the attribute to translate. For example, you can translate image title attribute as below,
     ```html
     <img [src]="example" i18n-title title="Internationlization" />
     ```
     By the way, you can also assign meaning, description and id with the i18n-x="<meaning>|<description>@@<id>" syntax.

     **[⬆ Back to Top](#table-of-contents)**

185. ### List down the pluralization categories?
     Pluralization has below categories depending on the language.
     1. =0 (or any other number)
     2. zero
     3. one
     4. two
     5. few
     6. many
     7. other

     **[⬆ Back to Top](#table-of-contents)**

186. ### What is select ICU expression?
     ICU expression is is similar to the plural expressions except that you choose among alternative translations based on a string value instead of a number. Here you define those string values.

     Let's take component binding with `residenceStatus` property which has "citizen", "permanent resident" and "foreigner" possible values and the message maps those values to the appropriate translations.
     ```javascript
     <span i18n>The person is {residenceStatus, select, citizen {citizen} permanent resident {permanentResident} foreigner {foreigner}}</span>
     ```

     **[⬆ Back to Top](#table-of-contents)**

187. ### How do you report missing translations?
     By default, When translation is missing, it generates a warning message such as "Missing translation for message 'somekey'". But you can configure with a different level of message in Angular compiler as below,
     1. **Error:** It throws an error. If you are using AOT compilation, the build will fail. But if you are using JIT compilation, the app will fail to load.
     2. **Warning (default):** It shows a 'Missing translation' warning in the console or shell.
     3. **Ignore:** It doesn't do anything.

     If you use AOT compiler then you need to perform changes in `configurations` section of your Angular CLI configuration file, angular.json.
     ```javascript
     "configurations": {
       ...
       "de": {
         ...
         "i18nMissingTranslation": "error"
       }
     }
     ```
     If you use the JIT compiler, specify the warning level in the compiler config at bootstrap by adding the 'MissingTranslationStrategy' property as below,
     ```javascript
     import { MissingTranslationStrategy } from '@angular/core';
     import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';
     import { AppModule } from './app/app.module';

     platformBrowserDynamic().bootstrapModule(AppModule, {
       missingTranslation: MissingTranslationStrategy.Error,
       providers: [
         // ...
       ]
     });
     ```
     **[⬆ Back to Top](#table-of-contents)**
188. ### How do you provide build configuration for multiple locales?
     You can provide build configuration such as translation file path, name, format and application url in `configuration` settings of Angular.json file. For example, the German version of your application configured the build as follows,
     ```javascript
     "configurations": {
       "de": {
         "aot": true,
         "outputPath": "dist/my-project-de/",
         "baseHref": "/fr/",
         "i18nFile": "src/locale/messages.de.xlf",
         "i18nFormat": "xlf",
         "i18nLocale": "de",
         "i18nMissingTranslation": "error",
       }
     ```

     **[⬆ Back to Top](#table-of-contents)**

189. ### What is an angular library?
     An Angular library is an Angular project that differs from an app in that it cannot run on its own. It must be imported and used in an app. For example,  you can import or add `service worker` library to an Angular application which turns an application into a Progressive Web App (PWA).

     **Note:** You can create own third party library and publish it as npm package to be used in an Application.

     **[⬆ Back to Top](#table-of-contents)**

190. ### What is AOT compiler?
     The AOT compiler is part of a build process that produces a small, fast, ready-to-run application package, typically for production. It converts your Angular HTML and TypeScript code into efficient JavaScript code during the build phase before the browser downloads and runs that code.

     **[⬆ Back to Top](#table-of-contents)**

191. ### How do you select an element in component template?
     You can control any DOM element via ElementRef by injecting it into your component's constructor. i.e, The component should have constructor with ElementRef parameter,
     ```javascript
     constructor(myElement: ElementRef) {
        el.nativeElement.style.backgroundColor = 'yellow';
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

195. ### How do you create schematics for libraries?
     You can create your own schematic collections to integrate your library with the Angular CLI. These collections are classified as 3 main schematics,
     1. **Add schematics:** These schematics are used to install library in an Angular workspace using `ng add` command.
        For example, @angular/material schematic tells the add command to install and set up Angular Material and theming.
     2. **Generate schematics**: These schematics are used to modify projects, add configurations and scripts, and scaffold artifacts in library using `ng generate` command.
        For example, @angular/material generation schematic supplies generation schematics for the UI components. Let's say the table component is generated using `ng generate @angular/material:table `.
     3. **Update schematics:** These schematics are used to update library's dependencies and adjust for breaking changes in a new library release using `ng update` command.
        For example, @angular/material update schematic updates material and cdk dependencies using `ng update @angular/material` command.

     **[⬆ Back to Top](#table-of-contents)**

196. ### How do you use jquery in Angular?
     You can use jquery in Angular using 3 simple steps,
     1. **Install the dependency:** At first, install the jquery dependency using npm
         ```cmd
            npm install --save jquery
         ```
     2. **Add the jquery script:** In Angular-CLI project, add the relative path to jquery in the angular.json file.
         ```javascript
         "scripts": [
            "node_modules/jquery/dist/jquery.min.js"
         ]
         ```
     3. **Start using jquery:** Define the element in template. Whereas declare the jquery variable and apply CSS classes on the element.
         ```html
         <div id="elementId">
           <h1>JQuery integration</h1>
         </div>
         ```
         ```javascript
         import {Component, OnInit} from '@angular/core';

         declare var $: any; // (or) import * as $ from 'jquery';

         @Component({
           selector: 'app-root',
           templateUrl: './app.component.html',
           styleUrls: ['./app.component.css']
         })
         export class AppComponent implements OnInit {
           ngOnInit(): void {
             $(document).ready(() => {
               $('#elementId').css({'text-color': 'blue', 'font-size': '150%'});
             });
           }
         }
         ```

     **[⬆ Back to Top](#table-of-contents)**

197. ### What is the reason for No provider for HTTP exception?
     This exception is due to missing HttpClientModule in your module. You just need to import in module as below,
     ```javascript
     import { HttpClientModule } from '@angular/common/http';

     @NgModule({
       imports: [
         BrowserModule,
         HttpClientModule,
       ],
       declarations: [ AppComponent ],
       bootstrap:    [ AppComponent ]
     })
     export class AppModule { }
     ```

     **[⬆ Back to Top](#table-of-contents)**

198. ### What is router state?
     The RouteState is an interface which represents the state of the router as a tree of activated routes.
     ```javascript
     interface RouterState extends Tree {
       snapshot: RouterStateSnapshot
       toString(): string
     }
     ```
     You can access the current RouterState from anywhere in the Angular app using the Router service and the routerState property.

     **[⬆ Back to Top](#table-of-contents)**

199. ### How can I use SASS in angular project?
     When you are creating your project with angular cli, you can use `ng new`command. It generates all your components with predefined sass files.
     ```javascript
     ng new My_New_Project --style=sass
     ```
     But if you are changing your existing style in your project then use `ng set` command,
     ```javascript
     ng set defaults.styleExt scss
     ```
     **[⬆ Back to Top](#table-of-contents)**

200. ### What is the purpose of hidden property?
     The hidden property is used  to show or hide the associated DOM element, based on an expression. It can be compared close to `ng-show` directive in AngularJS. Let's say you want to show user name based on the availability of user using `hidden` property.
     ```javascript
     <div [hidden]="!user.name">
       My name is: {{user.name}}
     </div>
     ```
     **[⬆ Back to Top](#table-of-contents)**

201. ### What is the difference between ngIf and hidden property?
     The main difference is that *ngIf will remove the element from the DOM, while [hidden] actually plays with the CSS style by setting `display:none`. Generally it is expensive to add and remove stuff from the DOM for frequent actions.

     **[⬆ Back to Top](#table-of-contents)**

202. ### What is slice pipe?
     The slice pipe is used to create a new Array or String containing a subset (slice) of the elements. The syntax looks like as below,
     ```javascript
     {{ value_expression | slice : start [ : end ] }}
     ```
     For example, you can provide 'hello' list based on a greeting array,
     ```javascript
     @Component({
       selector: 'list-pipe',
       template: `<ul>
         <li *ngFor="let i of greeting | slice:0:5">{{i}}</li>
       </ul>`
     })
     export class PipeListComponent {
       greeting: string[] = ['h', 'e', 'l', 'l', 'o', 'm','o', 'r', 'n', 'i', 'n', 'g'];
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

203. ### What is index property in ngFor directive?
     The index property of the NgFor directive is used to return the zero-based index of the item in each iteration. You can capture the index in a template input variable and use it in the template.

     For example, you can capture the index in a variable named indexVar and displays it with the todo's name using ngFor directive as below.
     ```javascript
     <div *ngFor="let todo of todos; let i=index">{{i + 1}} - {{todo.name}}</div>
     ```

     **[⬆ Back to Top](#table-of-contents)**

204. ### What is the purpose of ngFor trackBy?
     The main purpose of using *ngFor with trackBy option is performance optimization. Normally if you use NgFor with large data sets, a small change to one item by removing or adding an item, can trigger a cascade of DOM manipulations. In this case, Angular sees only a fresh list of new object references and to replace the old DOM elements with all new DOM elements. You can help Angular to track which items added or removed by providing a `trackBy` function which takes the index and the current item as arguments and needs to return the unique identifier for this item.

     For example, lets set trackBy to the trackByTodos() method
     ```javascript
     <div *ngFor="let todo of todos; trackBy: trackByTodos">
       ({{todo.id}}) {{todo.name}}
     </div>
     ```
     and define the trackByTodos method,
     ```javascript
     trackByTodos(index: number, item: Todo): number { return todo.id; }
     ```

     **[⬆ Back to Top](#table-of-contents)**

205. ### What is the purpose of ngSwitch directive?
     **NgSwitch** directive is similar to JavaScript switch statement which displays one element from among several possible elements, based on a switch condition. In this case only the selected element placed into the DOM. It has been used along with `NgSwitch`, `NgSwitchCase` and `NgSwitchDefault` directives.

     For example, let's display the browser details based on selected browser using ngSwitch directive.
     ```javascript
     <div [ngSwitch]="currentBrowser.name">
       <chrome-browser    *ngSwitchCase="'chrome'"    [item]="currentBrowser"></chrome-browser>
       <firefox-browser   *ngSwitchCase="'firefox'"     [item]="currentBrowser"></firefox-browser>
       <opera-browser     *ngSwitchCase="'opera'"  [item]="currentBrowser"></opera-browser>
       <safari-browser     *ngSwitchCase="'safari'"   [item]="currentBrowser"></safari-browser>
       <ie-browser  *ngSwitchDefault           [item]="currentItem"></ie-browser>
     </div>
     ```

     **[⬆ Back to Top](#table-of-contents)**

206. ### Is it possible to do aliasing for inputs and outputs?
     Yes, it is possible to do aliasing for inputs and outputs in two ways.
     1. **Aliasing in metadata:** The inputs and outputs in the metadata aliased using a colon-delimited (:) string with the directive property name on the left and the public alias on the right. i.e. It will be in the format of propertyName:alias.
         ```javascript
         inputs: ['input1: buyItem'],
         outputs: ['outputEvent1: completedEvent']
         ```
     2. **Aliasing with @Input()/@Output() decorator:** The alias can be specified for the property name by passing the alias name to the @Input()/@Output() decorator.i.e. It will be in the form of @Input(alias) or @Output(alias).
         ```javascript
         @Input('buyItem') input1: string;
         @Output('completedEvent') outputEvent1 = new EventEmitter<string>();
         ```

     **[⬆ Back to Top](#table-of-contents)**

207. ### What is safe navigation operator?
     The safe navigation operator(?)(or known as Elvis Operator) is used to guard against `null` and `undefined` values in property paths when you are not aware whether a path exists or not. i.e. It returns value of the object path if it exists, else it returns the null value.

     For example, you can access nested properties of a user profile easily without null reference errors as below,
     ```javascript
     <p>The user firstName is: {{user?.fullName.firstName}}</p>
     ```
     Using this safe navigation operator, Angular framework stops evaluating the expression when it hits the first null value and renders the view without any errors.

     **[⬆ Back to Top](#table-of-contents)**

208. ### Is any special configuration required for Angular9?
     You don't need any special configuration. In Angular9, the Ivy renderer is the default Angular compiler. Even though Ivy is available Angular8 itself, you had to configure it in tsconfig.json file as below,
     ```javascript
     "angularCompilerOptions": {    "enableIvy": true  }
     ```

     **[⬆ Back to Top](#table-of-contents)**

209. ### What are type safe TestBed API changes in Angular9?
     Angular 9 provides type safe changes in TestBed API changes by replacing the old get function with the new inject method. Because TestBed.get method is not type-safe. The usage would be as below,
     ```javascript
     TestBed.get(ChangeDetectorRef) // returns any. It is deprecated now.

     TestBed.inject(ChangeDetectorRef) // returns ChangeDetectorRef
     ```

     **[⬆ Back to Top](#table-of-contents)**

210. ### Is mandatory to pass static flag for ViewChild?
     In Angular 8, the static flag is required for ViewChild. Whereas in Angular9, you no longer need to pass this property. Once you updated to Angular9 using `ng update`, the migration will remove { static: false } script everywhere.
     ```javascript
     @ViewChild(ChildDirective) child: ChildDirective; // Angular9 usage
     @ViewChild(ChildDirective, { static: false }) child: ChildDirective; //Angular8 usage
     ```

     **[⬆ Back to Top](#table-of-contents)**

211. ### What are the list of template expression operators?
     The Angular template expression language supports three special template expression operators.
     1. Pipe operator
     2. Safe navigation operator
     3. Non-null assertion operator

     **[⬆ Back to Top](#table-of-contents)**

212. ### What is the precedence between pipe and ternary operators?
     The pipe operator has a higher precedence than the ternary operator (?:). For example, the expression `first ? second : third | fourth` is parsed as `first ? second : (third | fourth)`.

     **[⬆ Back to Top](#table-of-contents)**

213. ### What is an entry component?
     An entry component is any component that Angular loads imperatively(i.e, not referencing it in the template) by type. Due to this behavior, they can’t be found by the Angular compiler during compilation. These components created dynamically with `ComponentFactoryResolver`.

     Basically, there are two main kinds of entry components which are following -
     1. The bootstrapped root component
     2. A component you specify in a route

     **[⬆ Back to Top](#table-of-contents)**
214. ### What is a bootstrapped component?
     A bootstrapped component is an entry component that Angular loads into the DOM during the bootstrap process or application launch time. Generally, this bootstrapped or root component is named as `AppComponent` in your root module using `bootstrap` property as below.
     ```js
     @NgModule({
       declarations: [
         AppComponent
       ],
       imports: [
         BrowserModule,
         FormsModule,
         HttpClientModule,
         AppRoutingModule
       ],
       providers: [],
       bootstrap: [AppComponent] // bootstrapped entry component need to be declared here
     })
     ```

     **[⬆ Back to Top](#table-of-contents)**
215. ### How do you manually bootstrap an application?
     You can use `ngDoBootstrap` hook for a manual bootstrapping of the application instead of using bootstrap array in `@NgModule` annotation. This hook is part of `DoBootstrap` interface.
     ```js
     interface DoBootstrap {
       ngDoBootstrap(appRef: ApplicationRef): void
     }
     ```
     The module needs to be implement the above interface to use the hook for bootstrapping.
     ```js
     class AppModule implements DoBootstrap {
       ngDoBootstrap(appRef: ApplicationRef) {
         appRef.bootstrap(AppComponent); // bootstrapped entry component need to be passed
       }
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

216. ### Is it necessary for bootstrapped component to be entry component?
     Yes, the bootstrapped component needs to be an entry component. This is because the bootstrapping process is an imperative process.

     **[⬆ Back to Top](#table-of-contents)**

217. ### What is a routed entry component?
     The components referenced in router configuration are called as routed entry components. This routed entry component defined in a route definition as below,
     ```js
     const routes: Routes = [
       {
         path: '',
         component: TodoListComponent // router entry component
       }
     ];
     ```
     Since router definition requires you to add the component in two places (router and entryComponents), these components are always entry components.

     **Note:** The compilers are smart enough to recognize a router definition and automatically add the router component into `entryComponents`.

     **[⬆ Back to Top](#table-of-contents)**

218. ### Why is not necessary to use entryComponents array every time?
     Most of the time, you don't need to explicitly to set entry components in entryComponents array of ngModule decorator. Because angular adds components from both @NgModule.bootstrap and route definitions to entry components automatically.

     **[⬆ Back to Top](#table-of-contents)**

219. ### Do I still need to use entryComponents array in Angular9?
     No. In previous angular releases, the entryComponents array of ngModule decorator is used to tell the compiler which components would be created and inserted dynamically in the view. In Angular9, this is not required anymore with Ivy.

     **[⬆ Back to Top](#table-of-contents)**

220. ### Is it all components generated in production build?
     No, only the entry components and template components appears in production builds. If a component isn't an entry component and isn't found in a template, the tree shaker will throw it away. Due to this reason, make sure to add only true entry components to reduce the bundle size.

     **[⬆ Back to Top](#table-of-contents)**

221. ### What is Angular compiler?
     The Angular compiler is used to convert the application code into JavaScript code. It reads the template markup, combines it with the corresponding component class code, and emits component factories which creates JavaScript representation of the component along with elements of @Component metadata.

     **[⬆ Back to Top](#table-of-contents)**

222. ### What is the role of ngModule metadata in compilation process?
     The `@NgModule` metadata is used to tell the Angular compiler what components to be compiled for this module and how to link this module with other modules.

     **[⬆ Back to Top](#table-of-contents)**

223. ### How does angular finds components, directives and pipes?
     The Angular compiler finds a component or directive in a template when it can match the selector of that component or directive in that template. Whereas it finds a pipe if the pipe's name appears within the pipe syntax of the template HTML.

     **[⬆ Back to Top](#table-of-contents)**

224. ### Give few examples for NgModules?
     The Angular core libraries and third-party libraries are available as NgModules.
     1. Angular libraries such as FormsModule, HttpClientModule, and RouterModule are NgModules.
     2. Many third-party libraries such as Material Design, Ionic, and AngularFire2 are NgModules.

     **[⬆ Back to Top](#table-of-contents)**

225. ### What are feature modules?
     Feature modules are NgModules, which are used for the purpose of organizing code. The feature module can be created with Angular CLI using the below command in the root directory,
     ```javascript
     ng generate module MyCustomFeature //
     ```
     Angular CLI creates a folder called `my-custom-feature` with a file inside called `my-custom-feature.module.ts` with the following contents
     ```javascript
     import { NgModule } from '@angular/core';
     import { CommonModule } from '@angular/common';

     @NgModule({
       imports: [
         CommonModule
       ],
       declarations: []
     })
     export class MyCustomFeature { }
     ```

     **Note:**  The "Module" suffix shouldn't present in the name because the CLI appends it.

     **[⬆ Back to Top](#table-of-contents)**

226. ### What are the imported modules in CLI generated feature modules?
     In the CLI generated feature module, there are two JavaScript import statements at the top of the file
     1. **NgModule:** InOrder to use the `@NgModule` decorator
     2. **CommonModule:** It provides many common directives such as `ngIf` and `ngFor`.

     **[⬆ Back to Top](#table-of-contents)**

227. ### What are the differences between ngmodule and javascript module?
     Below are the main differences between Angular NgModule and javascript module,

     | NgModule | JavaScript module |
     |---- | --------- |
     | NgModule bounds declarable classes only | There is no restriction classes |
     | List the module's classes in declarations array only | Can define all member classes in one giant file |
     | It only export the declarable classes it owns or imports from other modules| It can export any classes |
     | Extend the entire application with services by adding providers to provides array | Can't extend the application with services |

     **[⬆ Back to Top](#table-of-contents)**

228. ### What are the possible errors with declarations?
     There are two common possible errors with declarations array,
     1. If you use a component without declaring it, Angular returns an error message.
     2. If you try to declare the same class in more than one module then compiler emits an error.

     **[⬆ Back to Top](#table-of-contents)**

229. ### What are the steps to use declaration elements?
     Below are the steps to be followed to use declaration elements.
     1. Create the element(component, directive and pipes) and export it from the file where you wrote it
     2. Import it into the appropriate module.
     3. Declare it in the @NgModule declarations array.


     **[⬆ Back to Top](#table-of-contents)**

230. ### What happens if browserModule used in feature module?
     If you do import `BrowserModule` into a lazy loaded feature module, Angular returns an error telling you to use `CommonModule` instead. Because BrowserModule’s providers are for the entire app so it should only be in the root module, not in feature module. Whereas Feature modules only need the common directives in CommonModule.

     ![ScreenShot](images/browser-module-error.gif)

     **[⬆ Back to Top](#table-of-contents)**

231. ### What are the types of feature modules?
     Below are the five categories of feature modules,
     1. **Domain:** Deliver a user experience dedicated to a particular application domain(For example, place an order, registration etc)
     2. **Routed:** These are domain feature modules whose top components are the targets of router navigation routes.
     3. **Routing:** It provides routing configuration for another module.
     4. **Service:** It provides utility services such as data access and messaging(For example, HttpClientModule)
     5. **Widget:** It makes components, directives, and pipes available to external modules(For example, third-party libraries such as Material UI)

     **[⬆ Back to Top](#table-of-contents)**

233. ### What is the recommendation for provider scope?
     You should always provide your service in the root injector unless there is a case where you want the service to be available only if you import a particular @NgModule.

     **[⬆ Back to Top](#table-of-contents)**

234. ### How do you restrict provider scope to a module?
     It is possible to restrict service provider scope to a specific module instead making available to entire application. There are two possible ways to do it.
     1. **Using providedIn in service:**
         ```js
         import { Injectable } from '@angular/core';
         import { SomeModule } from './some.module';

         @Injectable({
           providedIn: SomeModule,
         })
         export class SomeService {
         }
         ```
     2. **Declare provider for the service in module:**
         ```js
         import { NgModule } from '@angular/core';

         import { SomeService } from './some.service';

         @NgModule({
           providers: [SomeService],
         })
         export class SomeModule {
         }
         ```

     **[⬆ Back to Top](#table-of-contents)**

235. ### How do you provide a singleton service?
     There are two possible ways to provide a singleton service.
     1. Set the providedIn property of the @Injectable() to "root". This is the preferred way(starting from Angular 6.0) of creating a singleton service since it makes your services tree-shakable.

         ```js
         import { Injectable } from '@angular/core';

         @Injectable({
           providedIn: 'root',
         })
         export class MyService {
         }
         ```
     2. Include the service in root module or in a module that is only imported by root module. It has been used to register services before Angular 6.0.

         ```js
         @NgModule({
           ...
           providers: [MyService],
           ...
         })
         ```

     **[⬆ Back to Top](#table-of-contents)**

236. ### What are the different ways to remove duplicate service registration?
     If a module defines provides and declarations then loading the module in multiple feature modules will duplicate the registration of the service. Below are the different ways to prevent this duplicate behavior.
     1. Use the providedIn syntax instead of registering the service in the module.
     2. Separate your services into their own module.
     3. Define forRoot() and forChild() methods in the module.

     **[⬆ Back to Top](#table-of-contents)**

237. ### How does forRoot method helpful to avoid duplicate router instances?
     If the `RouterModule` module didn’t have forRoot() static method then each feature module would instantiate a new Router instance, which leads to broken application due to duplicate instances. After using forRoot() method, the root application module imports `RouterModule.forRoot(...)` and gets a Router, and all feature modules import `RouterModule.forChild(...)` which does not instantiate another Router.

     **[⬆ Back to Top](#table-of-contents)**

239. ### Can I share services using modules?
     No, it is not recommended to share services by importing module. i.e Import modules when you want to use directives, pipes, and components only. The best approach to get a hold of shared services is through 'Angular dependency injection' because importing a module will result in a new service instance.

     **[⬆ Back to Top](#table-of-contents)**

240. ### How do you get current direction for locales?
     In Angular 9.1, the API method `getLocaleDirection` can be used to get the current direction in your app. This method is useful to support Right to Left locales for your Internationalization based applications.
     ```js
     import { getLocaleDirection, registerLocaleData } from '@angular/common';
     import { LOCALE_ID } from '@angular/core';
     import localeAr from '@angular/common/locales/ar';

       ...

       constructor(@Inject(LOCALE_ID) locale) {

         const directionForLocale = getLocaleDirection(locale); // Returns 'rtl' or 'ltr' based on the current locale
         registerLocaleData(localeAr, 'ar-ae');
         const direction = getLocaleDirection('ar-ae'); // Returns 'rtl'

         // Current direction is used to provide conditional logic here
       }
     ```

     **[⬆ Back to Top](#table-of-contents)**

241. ### What is ngcc?
     The ngcc(Angular Compatibility Compiler) is a tool which upgrades node_module compiled with non-ivy ngc into ivy compliant format. The `postinstall` script from package.json will make sure your node_modules will be compatible with the Ivy renderer.
     ```js
     "scripts": {
        "postinstall": "ngcc"
     }
     ```

     Whereas, Ivy compiler (ngtsc), which compiles Ivy-compatible code.

     **[⬆ Back to Top](#table-of-contents)**

242. ### What classes should not be added to declarations?
     The below class types shouldn't be added to declarations
     1. A class which is already declared in any another module.
     2. Directives imported from another module.
     3. Module classes.
     4. Service classes.
     5. Non-Angular classes and objects, such as strings, numbers, functions, entity models, configurations, business logic, and helper classes.

     **[⬆ Back to Top](#table-of-contents)**

244. ### What is NoopZone?
     Zone is loaded/required by default in Angular applications and it helps Angular to know when to trigger the change detection. This way, it make sures developers focus on application development rather core part of Angular. You can also use Angular without Zone but the change detection need to be implemented on your own and `noop zone` need to be configured in bootstrap process.
     Let's follow the below two steps to remove zone.js,
     1. Remove the zone.js import from polyfills.ts.
         ```js
         /***************************************************************************************************
          * Zone JS is required by default for Angular itself.
          */
         // import 'zone.js/dist/zone';  // Included with Angular CLI.
         ```
     2. Bootstrap Angular with noop zone in src/main.ts.
         ```js
         platformBrowserDynamic().bootstrapModule(AppModule, {ngZone: 'noop'})
           .catch(err => console.error(err));
         ```
     **[⬆ Back to Top](#table-of-contents)**

245. ### How do you create displayBlock components?
     By default, Angular CLI creates components in an inline displayed mode(i.e, display:inline). But it is possible to create components with display: block style using `displayBlock` option,
     ```js
     ng generate component my-component --displayBlock
     ```
     (OR) the option can be turned on by default in Angular.json with `schematics.@schematics/angular:component.displayBlock` key value as true.

     **[⬆ Back to Top](#table-of-contents)**

246. ### What are the possible data update scenarios for change detection?
     The change detection works in the following scenarios where the data changes needs to update the application HTML.
     1. **Component initialization:** While bootstrapping the Angular application, Angular triggers the `ApplicationRef.tick()` to call change detection and View Rendering.
     2. **Event listener:**  The DOM event listener can update the data in an Angular component and trigger the change detection too.
         ```js
         @Component({
           selector: 'app-event-listener',
           template: `
             <button (click)="onClick()">Click</button>
             {{message}}`
         })
         export class EventListenerComponent {
           message = '';

           onClick() {
             this.message = 'data updated';
           }
         }
         ```
     3. **HTTP Data Request:** You can get data from a server through an HTTP request
         ```js
         data = 'default value';
         constructor(private httpClient: HttpClient) {}

           ngOnInit() {
             this.httpClient.get(this.serverUrl).subscribe(response => {
               this.data = response.data; // change detection will happen automatically
             });
           }
         ```
     4. **Macro tasks setTimeout() or setInterval():** You can update the data in the callback function of setTimeout or setInterval
         ```js
         data = 'default value';

           ngOnInit() {
             setTimeout(() => {
               this.data = 'data updated'; // Change detection will happen automatically
             });
           }
         ```
     5. **Micro tasks Promises:** You can update the data in the callback function of promise
         ```js
         data = 'initial value';

           ngOnInit() {
             Promise.resolve(1).then(v => {
               this.data = v; // Change detection will happen automatically
             });
           }
         ```
     6. **Async operations like Web sockets and Canvas:** The data can be updated asynchronously using WebSocket.onmessage() and Canvas.toBlob().

     **[⬆ Back to Top](#table-of-contents)**

247. ### What is a zone context?
      Execution Context is an abstract concept that holds information about the environment within the current code being executed. A zone provides an execution context that persists across asynchronous operations is called as zone context. For example, the zone context will be same in both outside and inside setTimeout callback function,
      ```js
      zone.run(() => {
        // outside zone
        expect(zoneThis).toBe(zone);
        setTimeout(function() {
          // the same outside zone exist here
          expect(zoneThis).toBe(zone);
        });
      });
      ```
      The current zone is retrieved through `Zone.current`.

     **[⬆ Back to Top](#table-of-contents)**

248. ### What are the lifecycle hooks of a zone?
     There are four lifecycle hooks for asynchronous operations from zone.js.
     1. **onScheduleTask:** This hook triggers when a new asynchronous task is scheduled. For example, when you call setTimeout()
         ```js
         onScheduleTask: function(delegate, curr, target, task) {
             console.log('new task is scheduled:', task.type, task.source);
             return delegate.scheduleTask(target, task);
           }
         ```
     2. **onInvokeTask:** This hook triggers when an asynchronous task is about to execute. For example, when the callback of setTimeout() is about to execute.
         ```js
         onInvokeTask: function(delegate, curr, target, task, applyThis, applyArgs) {
             console.log('task will be invoked:', task.type, task.source);
             return delegate.invokeTask(target, task, applyThis, applyArgs);
           }
         ```
     3. **onHasTask:** This hook triggers when the status of one kind of task inside a zone changes from stable(no tasks in the zone) to unstable(a new task is scheduled in the zone) or from unstable to stable.
         ```js
           onHasTask: function(delegate, curr, target, hasTaskState) {
             console.log('task state changed in the zone:', hasTaskState);
             return delegate.hasTask(target, hasTaskState);
           }
         ```
     4. **onInvoke:** This hook triggers when a synchronous function is going to execute in the zone.
         ```js
         onInvoke: function(delegate, curr, target, callback, applyThis, applyArgs) {
             console.log('the callback will be invoked:', callback);
             return delegate.invoke(target, callback, applyThis, applyArgs);
           }
         ```

     **[⬆ Back to Top](#table-of-contents)**

249. ### What are the methods of NgZone used to control change detection?
     NgZone service provides a `run()` method that allows you to execute a function inside the angular zone. This function is used to execute third party APIs which are not handled by Zone and trigger change detection automatically at the correct time.
     ```js
     export class AppComponent implements OnInit {
       constructor(private ngZone: NgZone) {}
       ngOnInit() {
         // use ngZone.run() to make the asynchronous operation in the angular zone
         this.ngZone.run(() => {
           someNewAsyncAPI(() => {
             // update the data of the component
           });
         });
       }
     }
     ```
     Whereas `runOutsideAngular()` method is used when you don't want to trigger change detection.
     ```js
     export class AppComponent implements OnInit {
       constructor(private ngZone: NgZone) {}
       ngOnInit() {
         // Use this method when you know no data will be updated
         this.ngZone.runOutsideAngular(() => {
           setTimeout(() => {
             // update component data and don't trigger change detection
           });
         });
       }
     }
     ```
     **[⬆ Back to Top](#table-of-contents)**

250. ### How do you change the settings of zonejs?
     You can change the settings of zone by configuring them in a separate file and import it just after zonejs import.
     For example, you can disable the requestAnimationFrame() monkey patch to prevent change detection for no data update as one setting and prevent DOM events(a mousemove or scroll event) to trigger change detection. Let's say the new file named zone-flags.js,
     ```js
     // disable patching requestAnimationFrame
     (window as any).__Zone_disable_requestAnimationFrame = true;

     // disable patching specified eventNames
     (window as any).__zone_symbol__UNPATCHED_EVENTS = ['scroll', 'mousemove'];
     ```
     The above configuration file can be imported in a polyfill.ts file as below,
     ```js
     /***************************************************************************************************
      * Zone JS is required by default for Angular.
      */
     import `./zone-flags`;
     import 'zone.js/dist/zone';  // Included with Angular CLI.
     ```
     **[⬆ Back to Top](#table-of-contents)**

251. ### How do you trigger an animation?
     Angular provides a `trigger()` function for animation in order to collect the states and transitions with a specific animation name, so that you can attach it to the triggering element in the HTML template. This function watch for changes and trigger initiates the actions when a change occurs.
     For example, let's create trigger named `upDown`, and attach it to the button element.
     ```js
     content_copy
     @Component({
       selector: 'app-up-down',
       animations: [
         trigger('upDown', [
           state('up', style({
             height: '200px',
             opacity: 1,
             backgroundColor: 'yellow'
           })),
           state('down', style({
             height: '100px',
             opacity: 0.5,
             backgroundColor: 'green'
           })),
           transition('up => down', [
             animate('1s')
           ]),
           transition('down => up', [
             animate('0.5s')
           ]),
         ]),
       ],
       templateUrl: 'up-down.component.html',
       styleUrls: ['up-down.component.css']
     })
     export class UpDownComponent {
       isUp = true;

       toggle() {
         this.isUp = !this.isUp;
       }

     ```

     **[⬆ Back to Top](#table-of-contents)**

252. ### How do you configure injectors with providers at different levels?
     You can configure injectors with providers at different levels of your application by setting a metadata value. The configuration can happen in one of three places,
     1. In the `@Injectable()` decorator for the service itself
     2. In the `@NgModule()` decorator for an NgModule
     3. In the `@Component()` decorator for a component

     **[⬆ Back to Top](#table-of-contents)**

253. ### Is it mandatory to use injectable on every service class?
     No. The `@Injectable()` decorator is not strictly required if the class has other Angular decorators on it or does not have any dependencies. But the important thing here is any class that is going to be injected with Angular is decorated.
     i.e, If we add the decorator, the metadata `design:paramtypes` is added, and the dependency injection can do it's job. That is the exact reason to add the @Injectable() decorator on a service if this service has some dependencies itself.
     For example, Let's see the different variations of AppService in a root component,
     1. The below AppService can be injected in AppComponent without any problems. This is because there are no dependency services inside AppService.
         ```js
         export class AppService {
           constructor() {
             console.log('A new app service');
           }
         }
         ```
     2. The below AppService with dummy decorator and httpService can be injected in AppComponent without any problems. This is because meta information is generated with dummy decorator.
         ```js
         function SomeDummyDecorator() {
           return (constructor: Function) => console.log(constructor);
         }

         @SomeDummyDecorator()
         export class AppService {
           constructor(http: HttpService) {
             console.log(http);
           }
         }
         ```
     and the generated javascript code of above service has meta information about HttpService,
         ```js
         var AppService = (function () {
             function AppService(http) {
                 console.log(http);
             }
             AppService = __decorate([
                 core_1.Injectable(),
                 __metadata('design:paramtypes', [http_service_1.HttpService])
             ], AppService);
             return AppService;
         }());
         exports.AppService = AppService;
         ```
     3. The below AppService with @injectable decorator and httpService can be injected in AppComponent without any problems. This is because meta information is generated with Injectable decorator.
         ```js
         @Injectable({
           providedIn: 'root',
         })
         export class AppService {
           constructor(http: HttpService) {
             console.log(http);
           }
         }
         ```
     **[⬆ Back to Top](#table-of-contents)**

254. ### What is an optional dependency?
     The optional dependency is a parameter decorator to be used on constructor parameters, which marks the parameter as being an optional dependency. Due to this, the DI framework provides null if the dependency is not found.
     For example, If you don't register a logger provider anywhere, the injector sets the value of logger(or logger service) to null in the below class.
     ```js
     import { Optional } from '@angular/core';

     constructor(@Optional() private logger?: Logger) {
       if (this.logger) {
         this.logger.log('This is an optional dependency message');
       } else {
         console.log('The logger is not registered');
       }
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

255. ### What are the types of injector hierarchies?
     There are two types of injector hierarchies in Angular

     1. **ModuleInjector hierarchy:** It configure on a module level using an @NgModule() or @Injectable() annotation.
     2. **ElementInjector hierarchy:** It created implicitly at each DOM element. Also it is empty by default unless you configure it in the providers property on @Directive() or @Component().

     **[⬆ Back to Top](#table-of-contents)**

257. ### What are dynamic forms?
     Dynamic forms is a pattern in which we build a form dynamically based on metadata that describes a business object model. You can create them based on reactive form API.
     **[⬆ Back to Top](#table-of-contents)**

259. ### What are the differences between reactive forms and template driven forms?
     Below are the main differences between reactive forms and template driven forms

     | Feature | Reactive | Template-Driven |
     |---- |---- | --------- |
     | Form model setup | Created(FormControl instance) in component explicitly | Created by directives  |
     | Data updates | Synchronous | Asynchronous |
     | Form custom validation | Defined as Functions | Defined as Directives |
     | Testing | No interaction with change detection cycle | Need knowledge of the change detection process |
     | Mutability | Immutable(by always returning new value for FormControl instance) | Mutable(Property always modified to new value) |
     | Scalability | More scalable using low-level APIs | Less scalable using due to abstraction on APIs|

     **[⬆ Back to Top](#table-of-contents)**


260. ### What are the different ways to group form controls?
     Reactive forms provide two ways of grouping multiple related controls.
     1. **FormGroup**: It defines a form with a fixed set of controls those can be managed together in an one object. It has same properties and methods similar to a FormControl instance.
        This FormGroup can be nested to create complex forms as below.
        ```js
        import { Component } from '@angular/core';
        import { FormGroup, FormControl } from '@angular/forms';

        @Component({
          selector: 'user-profile',
          templateUrl: './user-profile.component.html',
          styleUrls: ['./user-profile.component.css']
        })
        export class UserProfileComponent {
          userProfile = new FormGroup({
            firstName: new FormControl(''),
            lastName: new FormControl(''),
            address: new FormGroup({
                  street: new FormControl(''),
                  city: new FormControl(''),
                  state: new FormControl(''),
                  zip: new FormControl('')
                })
          });

          onSubmit() {
            // Store this.userProfile.value in DB
          }
        }
        ```
        ```html
        <form [formGroup]="userProfile" (ngSubmit)="onSubmit()">

          <label>
            First Name:
            <input type="text" formControlName="firstName">
          </label>

          <label>
            Last Name:
            <input type="text" formControlName="lastName">
          </label>

          <div formGroupName="address">
            <h3>Address</h3>

            <label>
              Street:
              <input type="text" formControlName="street">
            </label>

            <label>
              City:
              <input type="text" formControlName="city">
            </label>

            <label>
              State:
              <input type="text" formControlName="state">
            </label>

            <label>
              Zip Code:
              <input type="text" formControlName="zip">
            </label>
           </div>
            <button type="submit" [disabled]="!userProfile.valid">Submit</button>

        </form>
        ```
     2. **FormArray:** It defines a dynamic form in an array format, where you can add and remove controls at run time. This is useful for dynamic forms when you don’t know how many controls will be present within the group.
           ```js
            import { Component } from '@angular/core';
            import { FormArray, FormControl } from '@angular/forms';

            @Component({
              selector: 'order-form',
              templateUrl: './order-form.component.html',
              styleUrls: ['./order-form.component.css']
            })
            export class OrderFormComponent {
              constructor () {
                this.orderForm = new FormGroup({
                  firstName: new FormControl('John', Validators.minLength(3)),
                  lastName: new FormControl('Rodson'),
                  items: new FormArray([
                    new FormControl(null)
                  ])
                });
              }

              onSubmitForm () {
                // Save the items this.orderForm.value in DB
              }

              onAddItem () {
                this.orderForm.controls
                .items.push(new FormControl(null));
              }

              onRemoveItem (index) {
                this.orderForm.controls['items'].removeAt(index);
              }
            }
           ```
           ```html
           <form [formGroup]="orderForm" (ngSubmit)="onSubmit()">

             <label>
               First Name:
               <input type="text" formControlName="firstName">
             </label>

             <label>
               Last Name:
               <input type="text" formControlName="lastName">
             </label>

             <div>
             <p>Add items</p>
             <ul formArrayName="items">
               <li *ngFor="let item of orderForm.controls.items.controls; let i = index">
                 <input type="text" formControlName="{{i}}">
                 <button type="button" title="Remove Item" (click)="onRemoveItem(i)">Remove</button>
               </li>
             </ul>
             <button type="button" (click)="onAddItem">
               Add an item
             </button>
            </div>
           ```

     **[⬆ Back to Top](#table-of-contents)**

261. ### How do you update specific properties of a form model?
     You can use `patchValue()` method to update specific properties defined in the form model. For example,you can update the name and street of certain profile on click of the update button as shown below.
     ```js
     updateProfile() {
       this.userProfile.patchValue({
         firstName: 'John',
         address: {
           street: '98 Crescent Street'
         }
       });
     }
     ```
     ```html
       <button (click)="updateProfile()">Update Profile</button>
     ```

     You can also use `setValue` method to update properties.

     **Note:** Remember to update the properties against the exact model structure.

     **[⬆ Back to Top](#table-of-contents)**

262. ### What is the purpose of FormBuilder?
     FormBuilder is used as syntactic sugar for easily creating instances of a FormControl, FormGroup, or FormArray. This is helpful to reduce the amount of boilerplate needed to build complex reactive forms. It is available as an injectable helper class of the `@angular/forms` package.

     For example, the user profile component creation becomes easier as shown here.
     ```js
     export class UserProfileComponent {
       profileForm = this.formBuilder.group({
         firstName: [''],
         lastName: [''],
         address: this.formBuilder.group({
           street: [''],
           city: [''],
           state: [''],
           zip: ['']
         }),
       });
       constructor(private formBuilder: FormBuilder) { }
       }
     ```
     **[⬆ Back to Top](#table-of-contents)**

263. ### How do you verify the model changes in forms?
     You can add a getter property(let's say, diagnostic) inside component to return a JSON representation of the model during the development. This is useful to verify whether the values are really flowing from the input box to the model and vice versa or not.
     ```js
     export class UserProfileComponent {

       model = new User('John', 29, 'Writer');

       // TODO: Remove after the verification
       get diagnostic() { return JSON.stringify(this.model); }
     }
     ```
     and add `diagnostic` binding near the top of the form
     ```html
     {{diagnostic}}
     <div class="form-group">
       // FormControls goes here
     </div>
     ```

     **[⬆ Back to Top](#table-of-contents)**

264. ### What are the state CSS classes provided by ngModel?
     The ngModel directive updates the form control with special Angular CSS classes to reflect it's state. Let's find the list of classes in a tabular format,

     | Form control state | If true | If false |
     |---- | --------- | --- |
     | Visited | ng-touched | ng-untouched |
     | Value has changed | ng-dirty	 | ng-pristine |
     | Value is valid| 	ng-valid | ng-invalid |

     **[⬆ Back to Top](#table-of-contents)**

265. ### How do you reset the form?
     In a model-driven form, you can reset the form just by calling the function `reset()` on our form model.
     For example, you can reset the form model on submission as follows,
     ```js
     onSubmit() {
       if (this.myform.valid) {
         console.log("Form is submitted");
         // Perform business logic here
         this.myform.reset();
       }
     }
     ```
     Now, your form model resets the form back to its original pristine state.

     **[⬆ Back to Top](#table-of-contents)**

266. ### What are the types of validator functions?
     In reactive forms, the validators can be either synchronous or asynchronous functions,
     1. **Sync validators:** These are the synchronous functions which take a control instance and immediately return either a set of validation errors or null. Also, these functions passed as second argument while instantiating the form control. The main use cases are simple checks like whether a field is empty, whether it exceeds a maximum length etc.
     2. **Async validators:** These are the asynchronous functions which take a control instance and return a Promise or Observable that later emits a set of validation errors or null. Also, these functions passed as second argument while instantiating the form control. The main use cases are complex validations like hitting a server to check the availability of a username or email.

     The representation of these validators looks like below
     ```js
     this.myForm = formBuilder.group({
         firstName: ['value'],
         lastName: ['value', *Some Sync validation function*],
         email: ['value', *Some validation function*, *Some asynchronous validation function*]
     });
     ```

     **[⬆ Back to Top](#table-of-contents)**

267. ### Can you give an example of built-in validators?
     In reactive forms, you can use built-in validator like `required` and `minlength` on your input form controls. For example, the registration form can have these validators on name input field
     ```js
     this.registrationForm = new FormGroup({
         'name': new FormControl(this.hero.name, [
           Validators.required,
           Validators.minLength(4),
         ])
       });
     ```
     Whereas in template-driven forms, both `required` and `minlength` validators available as attributes.

     **[⬆ Back to Top](#table-of-contents)**

268. ### How do you optimize the performance of async validators?
     Since all validators run after every form value change, it creates a major impact on performance with async validators by hitting the external API on each keystroke. This situation can be avoided by delaying the form validity by changing the updateOn property from change (default) to submit or blur.
     The usage would be different based on form types,
     1. **Template-driven forms:** Set the property on `ngModelOptions` directive
         ```html
         <input [(ngModel)]="name" [ngModelOptions]="{updateOn: 'blur'}">
         ```
     2. **Reactive-forms:** Set the property on FormControl instance
         ```js
         name = new FormControl('', {updateOn: 'blur'});
         ```

     **[⬆ Back to Top](#table-of-contents)**

269. ### How to set ngFor and ngIf on the same element?
     Sometimes you may need to both ngFor and ngIf on the same element but unfortunately you are going to encounter below template error.
     ```cmd
      Template parse errors: Can't have multiple template bindings on one element.
     ```
      In this case, You need to use either ng-container or ng-template.
      Let's say if you try to loop over the items only when the items are available, the below code throws an error in the browser
      ```html
      <ul *ngIf="items" *ngFor="let item of items">
        <li></li>
      </ul>
      ```
      and it can be fixed by
      ```html
      <ng-container *ngIf="items">
        <ul *ngFor="let item of items">
          <li></li>
        </ul>
      </ng-container>
      ```

     **[⬆ Back to Top](#table-of-contents)**

270. ### What is host property in css?
     The `:host` pseudo-class selector is used to target styles in the element that hosts the component. Since the host element is in a parent component's template, you can't reach the host element from inside the component by other means.
     For example, you can create a border for parent element as below,
     ```js
     //Other styles for app.component.css
     //...
     :host {
       display: block;
       border: 1px solid black;
       padding: 20px;
     }
     ```
     **[⬆ Back to Top](#table-of-contents)**

271. ### How do you get the current route?
     In Angular, there is an `url` property of router package to get the current route. You need to follow the below few steps,

     1. Import Router from @angular/router
      ```js
        import { Router } from '@angular/router';
      ```
     2. Inject router inside constructor
      ```js
      constructor(private router: Router ) {

      }
      ```
     3. Access url parameter
      ```js
        console.log(this.router.url); //  /routename
      ```

      **[⬆ Back to Top](#table-of-contents)**

272. ### What is Component Test Harnesses?
     A component harness is a testing API around an Angular directive or component to make tests simpler by hiding implementation details from test suites. This can be shared between unit tests, integration tests, and end-to-end tests. The idea for component harnesses comes from the **PageObject** pattern commonly used for integration testing.

     **[⬆ Back to Top](#table-of-contents)**
     
273. ### What is the benefit of Automatic Inlining of Fonts?
     During compile time, Angular CLI will download and inline the fonts that your application is using. This performance update speed up the first contentful paint(FCP) and this feature is enabled by default in apps built with version 11.

     **[⬆ Back to Top](#table-of-contents)**

274. ### What is content projection?
     Content projection is a pattern in which you insert, or project, the content you want to use inside another component.

      **[⬆ Back to Top](#table-of-contents)**

277. ### How to create a standalone component uing CLI command?

      Generate standalone component using CLI command as shown below
      ```bash
      ng generate component component-name --standalone
      ```
      On running the command standalone component is created.
      Here is the list of file created.
      
      1. `component-name.component.ts`
      2. `component-name.component.css`
      3. `component-name.component.spec`
      4. `component-name.component.html`
      
      Next need to update `app.module.ts` as shown below.

      ```typescript
      import { NgModule } from '@angular/core';
      import { BrowserModule } from '@angular/platform-browser';
      import { ComponentNameComponent } from './component-name/component-name.component';

      @NgModule({
        imports: [
          BrowserModule,
          ComponentNameComponent
        ],
        declarations: [AppComponent],
        bootstrap: [AppComponent],
      })
      export class AppModule {}
      ```

      **[⬆ Back to Top](#table-of-contents)**

278. ### How to create a standalone component manually?
      To make existing component to standalone, then add `standalone: true` in `component-name.component.ts`
      as shown below

      ```typescript
      import { CommonModule } from '@angular/common';
      import { Component, OnInit } from '@angular/core';

      @Component({
        standalone: true,
        imports: [CommonModule],
        selector: 'app-standalone-component',
        templateUrl: './standalone-component.component.html',
        styleUrls: ['./standalone-component.component.css'],
      })
      export class ComponentNameComponent implements OnInit {
        constructor() {}

        ngOnInit() {}
      }
      ```
      Next need to update `app.module.ts` as shown below.

      ```typescript
      import { NgModule } from '@angular/core';
      import { BrowserModule } from '@angular/platform-browser';
      import { ComponentNameComponent } from './component-name/component-name.component';

      @NgModule({
        imports: [
          BrowserModule,
          ComponentNameComponent
        ],
        declarations: [AppComponent],
        bootstrap: [AppComponent],
      })
      export class AppModule {}
      ```
      
      **[⬆ Back to Top](#table-of-contents)**

279. ### What is hydration?
      Hydration is the process that restores the server side rendered application on the client. This includes things like reusing the server rendered DOM structures, persisting the application state, transferring application data that was retrieved already by the server, and other processes.

      To enable hydration, we have to enable server side rendering or Angular Universal. Once enabled, we can add the following piece of code in the root component.
        
      ```typescript
      import {
        bootstrapApplication,
        provideClientHydration,
      } from '@angular/platform-browser';

      bootstrapApplication(RootCmp, {
        providers: [provideClientHydration()]
      });
      ```
      Alternatively we can add `providers: [provideClientHydration()]` in the App Module
      ```typescript
      import {provideClientHydration} from '@angular/platform-browser';
      import {NgModule} from '@angular/core';
      ​
      @NgModule({
        declarations: [RootCmp],
        exports: [RootCmp],
        bootstrap: [RootCmp],
        providers: [provideClientHydration()],
      })
      export class AppModule {}
      ```
      
      **[⬆ Back to Top](#table-of-contents)**
  
281. ### Explain Angular Signals with an example. 
      In this example, we create a signal named `count` and initialize it with a value of 0. We then connect to the signal, allowing us to be notified whenever its value changes. Finally, we add a button that increments the count when clicked.

      When the button is clicked, the `incrementCount()` method is called. This method sets the new value of the `count` signal to 1. Objects connected to the signal (subscribers) are then notified of the change, and the updated value is displayed in the UI.

      In TypeScript file

      ```typescript
      import { Component, OnInit } from '@angular/core';
      import { signal, computed } from '@angular/core'; // Import from '@angular/core'

      @Component({
        selector: 'my-app',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css']
      })
      export class AppComponent implements OnInit {
        count = signal(0);
        doubleCount = computed(() => this.count() * 2);

        constructor() {}

        ngOnInit() {
          // Optional logging for debugging displayedCount changes
          // console.log('Displayed count changed to:', this.displayedCount());
        }

        incrementCount() {
          this.count.set(this.count() + 1);
        }

        decrementCount() {
          this.count.update((value) => Math.max(0, value - 1));
        }
      }
      ```
      In HTML file
      ```html
      <h1>Angular Signals Example</h1>

      <button (click)="incrementCount()" style="margin-right: 10px;">Increment Count</button>
      <button (click)="decrementCount()">Decrement Count</button>

      <p>Count: {{ count() }}</p>
      <p>Double Count: {{ doubleCount() }}</p>
      ```

      **[⬆ Back to Top](#table-of-contents)**

282. ### What are the Route Parameters? Could you explain each of them?.
      Route parameters are used to pass dynamic values in the URL of a route. They allow you to define variable segments in the route path, which can be accessed and used by components and services. Path parameters are represented by a colon (":") followed by the parameter name.

      There are three types of route parameters in Angular:

      **Path parameters:** Path parameters are used to define dynamic segments in the URL path. They are specified as part of the route's path and are extracted from the actual URL when navigating to that route. Path parameters are represented by a colon (":") followed by the parameter name. For example:

      ```typescript
      { path: 'users/:id', component: UserComponent }
      ```

      In this example, ":id" is the path parameter. When navigating to a URL like "/users/123", the value "123" will be extracted and can be accessed in the UserComponent.

      **Query parameters:** Query parameters are used to pass additional information in the URL as key-value pairs. They are appended to the URL after a question mark ("?") and can be accessed by components and services. Query parameters are not part of the route path, but they provide additional data to the route. For example:

      ```typescript
      { path: 'search', component: SearchComponent }
      ```

      In this example, a URL like "/search?query=angular" contains a query parameter "query" with the value "angular". The SearchComponent can retrieve the value of the query parameter and use it for searching.

      **Optional parameters:** Optional parameters are used when you want to make a route parameter optional. They are represented by placing a question mark ("?") after the parameter name. Optional parameters can be useful when you have routes with varying parameters. For example:

      ```typescript
      { path: 'products/:id/:category?', component: ProductComponent }
      ```

      In this example, the ":category" parameter is optional. The ProductComponent can be accessed with URLs like "/products/123" or "/products/123/electronics". If the ":category" parameter is present in the URL, it will be available in the component, otherwise, it will be undefined.

      Route parameters provide a flexible way to handle dynamic data in your Angular application. They allow you to create routes that can be easily customized and provide a seamless user experience by reflecting the current state of the application in the URL.

      **[⬆ Back to Top](#table-of-contents)**