# AngularExample

This project was generated with Angular CLI version 8.3.2.

Create an angular app and make the following changes to make it work with our shell.

1. In the shell we have use the tag <in-app> where our micro app is suppose to render and hence we will change the `app-root` in `src/app/app.component.ts` to `in-app`.

2. Inside `src/app/app.module.ts`, add base path to the providers.
```
import { NgModule } from "@angular/core";
import { APP_BASE_HREF } from "@angular/common";

@NgModule({
  ...
  providers: [{ provide: APP_BASE_HREF, useValue: "/angular" }],
})


```

3. We have set `/angular` as a base path so that when we hit URL with `/angular` from the shell, it will consider it as the base URL. If the URL in the shell is different for this app, update this base path accordingly.
