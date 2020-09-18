#### 全局管道

1. get.pipe.ts

```ts
import { Pipe, PipeTransform } from "@angular/core";
import { get } from "lodash";

// @example
// <h4>{{ data | get:'a.b' }}</h4>

@Pipe({
  name: "get"
})
export class GetPipe implements PipeTransform {
  transform(obj: object, path: string, default?): any {
    return get(obj, path, default);
  }
}

```

2. json2obj.pipe.ts

```ts
import { Pipe, PipeTransform } from "@angular/core";

// @example
// <ng-template [ngIf]="str | json2obj" let-value="ngIf">
// 	<h4>{{ value | json }}</h4>
// 	<h4>{{ value | get:'a' }}</h4>
// </ng-template>
// <ng-template [ngIf]=" null | json2obj" let-value="ngIf">
// 	我不会显示出来的
// </ng-template>

@Pipe({
  name: "json2obj",
})
export class Json2objPipe implements PipeTransform {
  transform(str: any): object {
    try {
      return JSON.parse(str);
    } catch (e) {
      return null;
    }
  }
}
```

3. safe-html.pipe.ts

```ts
import { Pipe, PipeTransform } from '@angular/core';
import { DomSanitizer } from '@angular/platform-browser';

@Pipe({
  name: 'safeHtml',
})
export class SafeHtmlPipe implements PipeTransform {
  constructor(private sanitized: DomSanitizer) {}
  transform(value: string) {
    return this.sanitized.bypassSecurityTrustHtml(value);
  }
}

```
