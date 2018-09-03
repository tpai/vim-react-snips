# Vim React Snippets

A Vim snippet library for React and it requires [UltiSnips](https://github.com/SirVer/ultisnips).

![demo](https://media.giphy.com/media/frXAXRdkvO32SqBij0/giphy.gif)

## Usage

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
" React snippets library
Plug 'tpai/vim-react-snips'

" Ultisnips
Plug 'SirVer/ultisnips'
```

Define trigger keys:

```vim
let g:UltiSnipsExpandTrigger="<c-f>"
let g:UltiSnipsJumpForwardTrigger="<c-l>"
let g:UltiSnipsJumpBackwardTrigger="<c-b>"
```

In insert mode

```
rapc<c-f>
```

Then it will expand to

```jsx
import React, { PureComponent } from 'react';
import PropTypes from 'prop-types';
import styles from './ComponentName.css';

class ComponentName extends PureComponent {
  static propTypes = {
    children: PropTypes.any,
  }
  static defaultProps = {
    children: null,
  }
  constructor(props) {
    super(props);
  }
  render() {
    const {
      children,
    } = this.props;

    return (
      <div className={styles['default']}>
        
      </div>
    );
  }
}

export default ComponentName;
```
