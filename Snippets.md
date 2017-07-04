# Snippets

## Checkbox

```html
<label className="check-ctrl">
  <input type="checkbox" value={this.state.isRemember} defaultChecked={isRemember}/>
  <span className="tx">Remember Password</span>
</label>
```

```css
/* check-ctrl */
.check-ctrl {
  position: relative;
  input[type="checkbox"] {
    position: absolute;
    left: 0;
    top: 0;
    opacity: 0;
  }
  input[type="checkbox"] ~ .tx {
    position: relative;
    padding-left: 26px;
    line-height: 16px;
    cursor: pointer;
    &:before {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      width: 15px;
      height: 15px;
      border-radius: 3px;
      background-color: rgb(172, 209, 140);
    }
  }
  input[type="checkbox"]:checked ~ .tx {
    &:after {
      content: '';
      background: url(../i/chk-tick.svg);
      position: absolute;
      left: 2px;
      top: 4px;
      z-index: 1;
      width: 11px;
      height: 7px;
      background-size: 11px 7px;
    }
  }
}
```

## Radio

```html
<label className="check-ctrl">
  <input type="radio" name="window" value={this.state.isOpen} defaultChecked={isOpen}/>
  <span className="tx">Remember Password</span>
</label>
```

```css
/* check-ctrl */
.check-ctrl {
  position: relative;
  input[type="radio"] {
    position: absolute;
    left: 0;
    top: 0;
    opacity: 0;
  }
  input[type="radio"] ~ .tx {
    position: relative;
    padding-left: 26px;
    line-height: 16px;
    cursor: pointer;
    &:before {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      width: 15px;
      height: 15px;
      border-radius: 3px;
      background-color: rgb(172, 209, 140);
    }
  }
  input[type="radio"]:checked ~ .tx {
    &:after {
      content: '';
      background: url(../i/chk-tick.svg);
      position: absolute;
      left: 2px;
      top: 4px;
      z-index: 1;
      width: 11px;
      height: 7px;
      background-size: 11px 7px;
    }
  }
}
```

