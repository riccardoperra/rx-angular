# Changelog

This file was generated using [@jscutlery/semver](https://github.com/jscutlery/semver).

## [0.0.0-beta.2](/compare/cdk@1.0.0-beta.1...cdk@1.0.0-beta.2) (2022-02-27)

### Bug Fixes

* **cdk:** compat for jest and Angular 12

# [1.0.0-beta.1](/compare/cdk@1.0.0-beat.1...cdk@1.0.0-beta.1) (2022-02-08)


### Bug Fixes

* **cdk:** use refCount in shareReplay 801d90f
* drop `@nrwl/tao` deep import 6eeae5e
* migrate `@rx-angular/zone-less` as well 78c1ec6
* **template:** Rxfor template typings (#1198) 5830f38, closes #1198


### Performance Improvements

* improve migrations perf 44eccda



# [1.0.0-beta.0](/compare/cdk@1.0.0-alpha.11...cdk@1.0.0-beta.0) (2022-02-02)


### Bug Fixes

* **cdk:** support rxjs 6 (#1183) 98749c8, closes #1183
* **docs:** adjust headline and add link to strategies 8bf672d
* **docs:** update strategyProvider docs f290142


### Features

* **docs:** add readme file to rxStrategyProvider 0675dac
* enable Ivy with partial compilation mode (#1186) eddaf20, closes #1186


### Performance Improvements

* move getUnpatchedApi into sun-package and avoid zone-less package (#1035) 170ab7a, closes #1035
* zone less sub modules f765336

### New zone-less sub entry points

With this version a migration was introduced, which migrates your codebase automatically to the new sub entry points.
run the migration:

```bash
ng update @rx-angular/cdk
// or
nx migrate @rx-angular/cdk
nx migrate --run-migrations
```

| item                      | from                          | to                                  |
|---------------------------|-------------------------------|-------------------------------------|
| `Promise`                 | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `requestAnimationFrame`   | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `cancelAnimationFrame`    | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `setInterval`             | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `clearInterval`           | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `setTimeout`              | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `clearTimeout`            | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `unpatchAddEventListener` | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/browser` |
| `interval`                | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `timer`                   | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `fromEvent`               | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `asyncScheduler`          | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `asapScheduler`           | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `queueScheduler`          | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |
| `animationFrameScheduler` | `@rx-angular/cdk/zone-less`   | `@rx-angular/cdk/zone-less/rxjs`    |

# [1.0.0-alpha.11](/compare/cdk@1.0.0-alpha.10...cdk@1.0.0-alpha.11) (2021-11-16)


### Bug Fixes

* **cdk-render-strategies:** don't send complete event to strategy-behavior (#954) 8df99ea, closes #954


### Features

* add ability to rxLet and push to take static values (#1033) 42d7a81, closes #1033

### New library structure

With this version a migration was introduced, which migrates your codebase automatically to the new sub entry points.
run the migration:

```bash
ng update @rx-angular/cdk
// or
nx migrate @rx-angular/cdk
nx migrate --run-migrations
```

| item                            | from              | to                                    |
|---------------------------------|-------------------|---------------------------------------|
| `RxCoalescingOptions`           | `@rx-angular/cdk` | `@rx-angular/cdk/coalescing`          |
| `coalescingObj`                 | `@rx-angular/cdk` | `@rx-angular/cdk/coalescing`          |
| `coalesceWith`                  | `@rx-angular/cdk` | `@rx-angular/cdk/coalescing`          |
| `coalescingManager`             | `@rx-angular/cdk` | `@rx-angular/cdk/coalescing`          |
| `CoalescingManager`             | `@rx-angular/cdk` | `@rx-angular/cdk/coalescing`          |
| `coerceObservable`              | `@rx-angular/cdk` | `@rx-angular/cdk/coercing`            |
| `coerceObservableWith`          | `@rx-angular/cdk` | `@rx-angular/cdk/coercing`            |
| `coerceDistinctObservable`      | `@rx-angular/cdk` | `@rx-angular/cdk/coercing`            |
| `coerceDistinctWith`            | `@rx-angular/cdk` | `@rx-angular/cdk/coercing`            |
| `coerceAllFactory`              | `@rx-angular/cdk` | `@rx-angular/cdk/coercing`            |
| `cancelCallback`                | `@rx-angular/cdk` | `@rx-angular/cdk/internals/scheduler` |
| `scheduleCallback`              | `@rx-angular/cdk` | `@rx-angular/cdk/internals/scheduler` |
| `forceFrameRate`                | `@rx-angular/cdk` | `@rx-angular/cdk/internals/scheduler` |
| `PriorityLevel`                 | `@rx-angular/cdk` | `@rx-angular/cdk/internals/scheduler` |
| `RxStrategyProvider`            | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `ScheduleOnStrategyOptions`     | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RX_CONCURRENT_STRATEGIES`      | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxConcurrentStrategies`        | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RX_NATIVE_STRATEGIES`          | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxNativeStrategies`            | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `onStrategy`                    | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `strategyHandling`              | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxStrategies`                  | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxStrategyNames`               | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxDefaultStrategyNames`        | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxConcurrentStrategyNames`     | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxNativeStrategyNames`         | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxCustomStrategyCredentials`   | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxStrategyCredentials`         | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxRenderBehavior`              | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxRenderWork`                  | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RX_ANGULAR_CONFIG`             | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RX_ANGULAR_DEFAULTS`           | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `RxAngularConfig`               | `@rx-angular/cdk` | `@rx-angular/cdk/render-strategies`   |
| `ObservableAccumulation`        | `@rx-angular/cdk` | `@rx-angular/cdk/internals/core`      |
| `ObservableMap`                 | `@rx-angular/cdk` | `@rx-angular/cdk/internals/core`      |
| `accumulateObservables`         | `@rx-angular/cdk` | `@rx-angular/cdk/internals/core`      |
| `getZoneUnPatchedApi`           | `@rx-angular/cdk` | `@rx-angular/cdk/internals/core`      |
| `templateHandling`              | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxBaseTemplateNames`           | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxRenderAware`                 | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxViewContext`                 | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `rxBaseTemplateNames`           | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxTemplateManager`             | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `createTemplateManager`         | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxNotificationTemplateNameMap` | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxListManager`                 | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `createListTemplateManager`     | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxListViewComputedContext`     | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxDefaultListViewContext`      | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxListViewContext`             | `@rx-angular/cdk` | `@rx-angular/cdk/template`            |
| `RxNotificationKind`            | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxNotification`                | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxCompleteNotification`        | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxErrorNotification`           | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxNextNotification`            | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxNotificationValue`           | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `RxSuspenseNotification`        | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `toRxErrorNotification`         | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `toRxSuspenseNotification`      | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `toRxCompleteNotification`      | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `templateTriggerHandling`       | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `rxMaterialize`                 | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `createTemplateNotifier`        | `@rx-angular/cdk` | `@rx-angular/cdk/notifications`       |
| `Promise`                       | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `requestAnimationFrame`         | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `cancelAnimationFrame`          | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `setInterval`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `clearInterval`                 | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `setTimeout`                    | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `clearTimeout`                  | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `unpatchAddEventListener`       | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `interval`                      | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `timer`                         | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `fromEvent`                     | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `asyncScheduler`                | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `asapScheduler`                 | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `queueScheduler`                | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `animationFrameScheduler`       | `@rx-angular/cdk` | `@rx-angular/cdk/zone-less`           |
| `focusEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `mouseEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `wheelEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `inputEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `formControlsEvents`            | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `keyboardEvents`                | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `vrEvents`                      | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `mSGestureEvents`               | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `printEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `networkEvents`                 | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `audioEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `compositionEvents`             | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `touchEvents`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `globalEvents`                  | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `websocketEvents`               | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `xhrEvents`                     | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `windowEvents`                  | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `allEvents`                     | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `EventTarget`                   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `RxZoneFlagsHelperFunctions`    | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `RxZoneGlobalConfigurations`    | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `RxZoneTestConfigurations`      | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `RxZoneRuntimeConfigurations`   | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |
| `zoneConfig`                    | `@rx-angular/cdk` | `@rx-angular/cdk/zone-configurations` |



# [1.0.0-alpha.10](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.9...cdk@1.0.0-alpha.10) (2021-08-23)

* **cdk:** fix RxJS7 update ([#907](https://github.com/rx-angular/rx-angular/pull/907)) ([674d584]()


# [1.0.0-alpha.9](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.7...cdk@1.0.0-alpha.9) (2021-08-16)


### Bug Fixes

* **cdk:** setup polyfills for non browser environments in scheduler ([#820](https://github.com/rx-angular/rx-angular/issues/820)) ([674d584](https://github.com/rx-angular/rx-angular/commit/674d5847d709380d6e6bee6e5e230ae36b688818))
* **cdk:** skip logging irelevant browser API error ([#741](https://github.com/rx-angular/rx-angular/issues/741)) ([78a624f](https://github.com/rx-angular/rx-angular/commit/78a624f993a63327ffce2fcd4ce032d693deb129))
* **demos:** fix most of the demos ([#640](https://github.com/rx-angular/rx-angular/issues/640)) ([3d443e9](https://github.com/rx-angular/rx-angular/commit/3d443e927ccc90f2bc7919c7364e3f3ab5cb8595))

### Features

* **cdk:** add accumulateObservable creation function ([#582](https://github.com/rx-angular/rx-angular/issues/582)) ([65250ba](https://github.com/rx-angular/rx-angular/commit/65250ba15ab2c6569a00b0d82c57be9ba54787c8))
* **cdk:** improve rendering error handling ([#626](https://github.com/rx-angular/rx-angular/issues/626)) ([0437438](https://github.com/rx-angular/rx-angular/commit/0437438112c42b8f072b219d599d5ea8d68b30bc))
* **cdk:** move scheduler into `internals/scheduler` ([#725](https://github.com/rx-angular/rx-angular/issues/725)) ([26aedbd](https://github.com/rx-angular/rx-angular/commit/26aedbd5c3f78e65d40797e3c310e797f00c426f))
* **cdk:** swap arguments in the `getZoneUnPatchedApi` to benefit from autocomplete ([#707](https://github.com/rx-angular/rx-angular/issues/707)) ([6d5341d](https://github.com/rx-angular/rx-angular/commit/6d5341d22d5e24bf55289654989d3c11dd47c1e8))
* **zone-configuration:** add ts docs to zone configuration ([#667](https://github.com/rx-angular/rx-angular/issues/667)) ([da4eb77](https://github.com/rx-angular/rx-angular/commit/da4eb776747c0e812e2fea1c4eac533db71d04cb))
* **coercing:** add ts docs to coercing 
* **coalescing:** add ts docs to coalescing 


### Performance Improvements

* **cdk:** decouple `notifications` into a lib ([#782](https://github.com/rx-angular/rx-angular/issues/782)) ([3032b69](https://github.com/rx-angular/rx-angular/commit/3032b696a909bd9066572584fd2fbb1a132fb730))
* **cdk:** decouple `zone-configurations` into its own library ([#728](https://github.com/rx-angular/rx-angular/issues/728)) ([4f35bfa](https://github.com/rx-angular/rx-angular/commit/4f35bfaf2a65333b3eff2f74671ad2c443946ca4))
* **cdk:** decouple `zone-less` into its own self-contained library ([#688](https://github.com/rx-angular/rx-angular/issues/688)) ([bf561e8](https://github.com/rx-angular/rx-angular/commit/bf561e837b37c25ae2ce5430eb861f08ec9c0204))
* **cdk:** move `coercing` into lib ([#730](https://github.com/rx-angular/rx-angular/issues/730)) ([803412b](https://github.com/rx-angular/rx-angular/commit/803412b8f00d1e0b31f07ced1a2951e445b48546))
* **cdk:** use existing `rxjs` schedulers ([#700](https://github.com/rx-angular/rx-angular/issues/700)) ([15d0333](https://github.com/rx-angular/rx-angular/commit/15d0333d74b4da56407a7514f2cc50b7db82c93d))


# [1.0.0-alpha.8](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.7...cdk@1.0.0-alpha.8) (2021-04-13)

### Features

- **cdk:** improve rendering error handling ([#626](https://github.com/rx-angular/rx-angular/issues/626)) ([0437438](https://github.com/rx-angular/rx-angular/commit/0437438112c42b8f072b219d599d5ea8d68b30bc))

# [1.0.0-alpha.7](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.6...cdk@1.0.0-alpha.7) (2021-03-27)

### Bug Fixes

- **cdk, template:** remove window object access ([#599](https://github.com/rx-angular/rx-angular/issues/599)) ([47b6dbb](https://github.com/rx-angular/rx-angular/commit/47b6dbb66deac7b44cb7aa0f348bc45cd64541fb)), closes [#579](https://github.com/rx-angular/rx-angular/issues/579)

### Features

- **cdk:** infer `getZoneUnPatchedApi` return type and fix types for existing functions ([#603](https://github.com/rx-angular/rx-angular/issues/603)) ([1692653](https://github.com/rx-angular/rx-angular/commit/1692653c8c6cada97fb37af176ca9a41ef93e35d))
- **zone-config:** update zone-config docs and linking ([#627](https://github.com/rx-angular/rx-angular/issues/627)) ([adb613d](https://github.com/rx-angular/rx-angular/commit/adb613daed5767e184135ddd2efe48fa9522a5dd))

# [1.0.0-alpha.6](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.4...cdk@1.0.0-alpha.6) (2021-03-14)

### Bug Fixes

- **zone-config:** Update zone cfg api ([#598](https://github.com/rx-angular/rx-angular/issues/598)) ([8dadf40](https://github.com/rx-angular/rx-angular/commit/8dadf40007c85c8794d21317a702a743100fc1c2))
- **zone-config:** zone-config tests ([#600](https://github.com/rx-angular/rx-angular/issues/600)) ([517e0cf](https://github.com/rx-angular/rx-angular/commit/517e0cf55e38e068c9127395395d1cc63b7b405b))
- **list-manager:** fix list manager return value when no changes happened but values arrived ([#588](https://github.com/rx-angular/rx-angular/issues/588)) ([220be51](https://github.com/rx-angular/rx-angular/commit/220be517d65fc70f851cc3a24bddcd28251d85dd))

# [1.0.0-alpha.5](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.4...cdk@1.0.0-alpha.5) (2021-03-10)

### Bug Fixes

- Fix change detection not running inside the zone when `patchZone` is truthy https://github.com/rx-angular/rx-angular/pull/590
  This change should fix a lot of cdnage detection issues related to event listeners. Special THX to @arturovt

# [1.0.0-alpha.4](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.2...cdk@1.0.0-alpha.4) (2021-02-27)

### Bug Fixes

- ng-packagr builds ([#553](https://github.com/rx-angular/rx-angular/issues/553)) ([cfd4711](https://github.com/rx-angular/rx-angular/commit/cfd47112c12bf7333e657c2f6b6e79d3d3eccda4))
- update typings, allow values in template slots

### Features

- **cdk:** improve template manager view-context ([#561](https://github.com/rx-angular/rx-angular/issues/561)) ([f58b9a2](https://github.com/rx-angular/rx-angular/commit/f58b9a2f147f3ca3cd89038a4603bd2ea0f2fe25))

# [1.0.0-alpha.3](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.2...cdk@1.0.0-alpha.3) (2021-02-24)

### Bug Fixes

- **cdk:** ng-packagr builds ([#553](https://github.com/rx-angular/rx-angular/issues/553)) ([cfd4711](https://github.com/rx-angular/rx-angular/commit/cfd47112c12bf7333e657c2f6b6e79d3d3eccda4))
  removed imports and dependencies to scheduler

# [1.0.0-alpha.2](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.0...cdk@1.0.0-alpha.2) (2021-02-23)

### Bug Fixes

- **cdk:** add scheduler

# [1.0.0-alpha.1](https://github.com/rx-angular/rx-angular/compare/cdk@1.0.0-alpha.0...cdk@1.0.0-alpha.1) (2021-02-22)

### Bug Fixes

- **cdk:** adopt build ([cbc59d3](https://github.com/rx-angular/rx-angular/commit/cbc59d3b05032154ef7829822a6d5fd59ce82010))
- **cdk:** fix build ([e9b6d2d](https://github.com/rx-angular/rx-angular/commit/e9b6d2d51e85d25335f6ded794450df860badaca))

### Features

- **cdk:** harmonize API ([#548](https://github.com/rx-angular/rx-angular/issues/548)) ([054d3e5](https://github.com/rx-angular/rx-angular/commit/054d3e573fc305f0b51e9f48c8dcb85554bf532f))

# 1.0.0-alpha.0 (2021-02-21)

### Bug Fixes

- **cdk:** adopt build ([cbc59d3](https://github.com/rx-angular/rx-angular/commit/cbc59d3b05032154ef7829822a6d5fd59ce82010))
- **cdk:** fix build ([e9b6d2d](https://github.com/rx-angular/rx-angular/commit/e9b6d2d51e85d25335f6ded794450df860badaca))

### Features

- **cdk:** add zone-config ([#492](https://github.com/rx-angular/rx-angular/issues/492)) ([35f2d9b](https://github.com/rx-angular/rx-angular/commit/35f2d9b703401552318f6be665f3442212e43ae1))
- **cdk:** docs and tests ([ce29d15](https://github.com/rx-angular/rx-angular/commit/ce29d15916c676b29d5159121d35605cbcc96885))
- **cdk:** setup render-strategies and template-management ([#489](https://github.com/rx-angular/rx-angular/issues/489)) ([8cbcdbd](https://github.com/rx-angular/rx-angular/commit/8cbcdbde2283327d3a6b404f564b46751f039d1b))
