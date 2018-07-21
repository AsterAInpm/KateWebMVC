#Typescript based web MVC framework


    npm  i kate-web-mvc typescript @types/node express
    
### example

```typescript

import { KateWebApp, action } from 'kate-web-mvc';


class IndexController {

  @action('/') // express compatible route
  someIndexAction(req): string {
    return JSON.stringify({
      field_1: 'value_122',
      field_2: 'value_2',
    })
  }

}

// register controller
KateWebApp.addController(new IndexController());

const port = process.env.PORT || 3000;
KateWebApp.run(port);


```
then run `tsc` compiler 

