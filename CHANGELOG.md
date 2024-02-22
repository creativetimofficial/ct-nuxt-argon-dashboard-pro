# Changelog

## [2.1.0] 2024-02-22

- Update dependencies & devDependencies
- Add `Pinia` for state management.
- Add slider component to `smart-home` using `vue3-slider`
- Fix Sidebar issue on Mobile
- Fix navbar notification menu issue
- Fix issues that reloaded pages on each route change

## [2.0.0] 2022-12-06

- Fix errors
- Update dependencies
- Add new components
- Add new pages and layouts
- Add new design blocks
- Add vuex to the project
- New base strucuture for more reusable components

## [1.4.0] - 2021-10-22

- ### Updates
- All dependencies updated to the latest version
- Perfect Scrollbar fix on windows devices
- `Node-sass` package remove because now is deprecated
- Add `Sass` package
- To get rid of the annoying warnings and solve them run in your command line first `npm install -g sass-migrator` and after that run `sass-migrator division **/*.scss`

## [1.3.0] - 2021-02-25

### Updates

- All dependencies updated to the latest version
- Vee Validate was updated to latest version of V3
- Vuejs was update to latest version of V2
- Bootstrap version remains the same because they have an error on the latest 4.6.0 version and the compile is not possible

## [1.2.1] - 2020-02-21

- Improvements and fixes for BaseInput component
- Add validation states for other components such as checkboxes, radio, html editor when they are used with BaseInput as wrapper
- Lock some dependencies to avoid styling issues (dropzone, bootstrap etc)
- Upgrade some packages
-

## [1.2.0] - 2020-01-05

- Improve tags input styles on mobile
- Alternative input style fixes
- Update sweet alert
- Lock bootstrap version to 4.3.1
- Modal click outside improvements
- Pie chart tooltip improvements
- Prevent enter key on tags input
- Fix sidebar scroll issue
- Fix sidebar resize issues
- Upgrade vee-validate to version 3. Update form validation code to vee validate 3
- Fix ActivityFeed component import issue

### Upgrade tips

- Copy over _components_ folder and _assets_ folder.
- Copy _dashboard-plugin.js_ and _globalComponents.js_ files.
- Add this code under `build` option in nuxt.config.js

```js
transpile: ["vee-validate/dist/rules"];
```

- Diff the package.json with yours to see which packages were upgraded.
- In your code, if you used the old vee-validate with `v-validate` directive, change it like this

This code

```html
<base-input
  v-validate="'required'"
  name="First Name"
  :error="getError('First Name')"
>
</base-input>
```

should be changed to

```{1}html
<base-input rules="required" name="First Name">
</base-input>
```

The `base-input` component can be used as a wrapper to validate any other custom component now.
For example, validating an element-ui select:

```{1}html
<base-input rules="required" name="My select">
 <el-select v-model="someValue">
 </el-select>
</base-input>
```

For more details check [Migration guide from vee-validate](https://logaretm.github.io/vee-validate/migration.html#migrating-from-2-x-to-3-0)

## [1.1.1] - 2019-10-14

### Bug fixes & improvements

- Improve sidebar behaviour when resizing from desktop to mobile and vice-versa
- Fix checkbos/radio related issue after full page refresh

## [1.1.0] - 2019-08-28

### Bug fixes & improvements

- Add special no ssr plugins for full calendar and vector maps
- Bug fixes for navbar & tables
- Code cleanups

## [1.0.0] - 2019-07-04

### Initial Release
