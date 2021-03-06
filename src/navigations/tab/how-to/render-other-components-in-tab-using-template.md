---
title: "Render other components in Tab using template"
component: "Accordion"
description: "This example demonstrates how to render other Essential JS 2 components into Essential JS 2 Tab component content using template."
---

# Render other components in Tab using template

You can render other components inside Tab using React **template**. Through this, we can add content as other components directly with all functionalities to our Tab. Follow the below guidelines for using the other components as template in tab.

* Declare a template within the function returns jsx element. If the template does not need arguments no need to pass the properties.

* Assign the function as value for the template property.

{% tab template="tab/direct-components", isDefaultActive=true, compileJsx=true %}

```typescript

import * as React from 'react';
import * as ReactDOM from 'react-dom';
import { TabComponent, TabItemDirective, TabItemsDirective, SelectEventArgs } from '@syncfusion/ej2-react-navigations';
import {ButtonComponent} from '@syncfusion/ej2-react-buttons';
import { DatePickerComponent ,CalendarComponent} from '@syncfusion/ej2-react-calendars';


export default class App extends React.Component<{}, {}> {

  render() {
  let headertext: any;
  function contentTemplate(): JSX.Element {
    return(<ButtonComponent>Click me</ButtonComponent>);
  }
  function contentTemplate1(): JSX.Element {
    return(<DatePickerComponent></DatePickerComponent>);
  }
  function contentTemplate2(): JSX.Element {
    return( <CalendarComponent ></CalendarComponent>);
  }
    headertext = [{ text: "Tab1"}, { text: "Tab2"}, { text: "Tab3"}];
    return (
        <div id='container'>
          <TabComponent heightAdjustMode='Auto' id='tabelement'>
            <TabItemsDirective>
              <TabItemDirective header= { headertext[0] }
                content= { contentTemplate } />
            <TabItemDirective header= { headertext[1] }
                content= { contentTemplate1 } />
          <TabItemDirective header= { headertext[2] }
                content= { contentTemplate2 } />
            </TabItemsDirective>
          </TabComponent>
        </div>
    );
  }
}

ReactDOM.render(<App />, document.getElementById('element'));

```

{% endtab %}