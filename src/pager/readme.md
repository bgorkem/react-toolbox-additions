# Pager

Provides functionality of pagination control, actually the component is not defined at(https://www.google.com/design/spec/components), 
but designed by using standard components from material design utilizing react-toolbox components library (http://react-toolbox.com/). 
It is easy to use and configure, also it is highly customizable.

<!-- example -->
```jsx
import Pager from 'react-toolbox-additions/lib/pager';
import FontIcon from 'react-toolbox-additions/lib/font_icon';

const PagerTest = () => {

    onPageChange = (newPage, oldPage) => {
      console.info('Selected page : ' + newPage + ', Previous page: ' + oldPage);
    }

    return (
      <Pager 
        prevButtonLabel={ (<FontIcon value='chevron_left' />) }
        nextButtonLabel={ (<FontIcon value='chevron_right' />) }
        rangeLeftButtonLabel={(<FontIcon value='more_horiz' />)}
        rangeRightButtonLabel={(<FontIcon value='more_horiz' />)}
        totalPages={29}
        currentPage={5}
        visiblePagesBlockSize={3}
        onPageChange={onPageChange}
      />
  );
};
```

If you want to provide a theme via context, the component key is `ERTPager`.

## Properties

| Name          | Type        | Default         | Description|
|:-----|:-----|:-----|:-----|
| `prevButtonLabel`                 | `String`    | `\u003C`            | Used for the previous button label content, it can be text or FontIcon element.|
| `nextButtonLabel`                 | `String`    | `\u003E`            | Used for the next button label content, it can be text or FontIcon element.|
| `rangeLeftButtonLabel`            | `String`    | `...`               | Used for the left range button label content, it can be text or FontIcon element.|
| `rangeRightButtonLabel`           | `String`    | `...`               | Used for the right range button label content, it can be text or FontIcon element.|
| `currentPage`                     | `Number`    | `1`                 | A Number with the currently selected page.|
| `totalPages`                      | `Number`    | `1`                 | A Number of total pages.|
| `visiblePagesBlockSize`           | `Number`    | `3`                 | A Number of pages visible in control except next, previous and ranges buttons, the minimum value is 2.|
| `onPageChange`                    | `Function`  |                     | Callback called when the page is changing.|
| `theme`                           | `String`    |                     | Classnames object defining the component style.|
| `pagerClassName`                  | `String`    |                     | This class will be applied to the root elemt.|
| `firstLastPagesButtonStyles`      | `Object`    | {raised: true}      | Defining default style of first and last page buttons.|
| `leftRightArrowButtonStyles`      | `Object`    | {raised: true}      | Defining default style of next and previous arrow buttons.|
| `leftRightRangeButtonStyles`      | `Object`    | {flat: true}        | Defining default style of left and right range buttons.|
| `pagesButtonStyles`               | `Object`    | {flat: true}        | Defining default style of regular pages buttons.|


## Theme

| Name     | Description|
|:---------|:-----------|
| `pager`                 | Used for the root element.|
| `active`                | Used for the active page.|
| `firstLastPagesButton`  | Used for the first and last arrow buttons.|
| `leftRightArrowButton`  | Used for the next and previous arrow buttons.|
| `leftRightRangeButton`  | Used for the next and previous range pages buttons.|
| `pagesButton`           | Used for the regular pages buttons.|