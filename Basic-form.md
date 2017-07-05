## Basic form

```html
<form className="form">
    <div className="form-group">
      <label className="required" htmlFor="st">Project Title</label>
      <div className="v">
        <input type="text" className="input-text" id="st" placeholder="Sort Title" />
      </div>
    </div>
    
    <div className="form-group">
      <label htmlFor="td">Required Due Date/ Estimated Timeline</label>
      <div className="v">
        <DatePicker selected={this.state.targetDate} onChange={this.handleChange} className="input-text datepicker" placeholderText="Target Date" />
      </div>
    </div>

    <div className="form-group">
      <label className="required" htmlFor="st">Select the Functional area from which this request originated </label>
      <div className="v">
        <Select name="form-field-name" value={this.state.functionalArea} options={functionalAreaOptions} onChange={this.functionalAreaChange} placeholder="Request Origin" className="input-select" />
      </div>
  </div>
</form>
```

```css
.form-group {
  label {
    display: block;
    font-size: 14px;
    color: #312626;
    font-weight: normal;
    position: relative;
    &.required {
      padding-left: 10px;
      &:before {
        content: '*';
        color: #238a58;
        font-size: 14px;
        position: absolute;
        left: 0;
        top: 0;
      }
    }
  }
  label ~ .v {
    margin-top: 13px;
    margin-bottom: 32px;
  }
  label +.v-smo {
    width: 142px;
  }
  label +.v-sm {
    width: 142px;
    margin-bottom: 13px;
  }
  @include input-placeholder {
    color: #999;
  }
  .input-text {
    font-size: 14px;
    padding: 0 16px;
    color: #312626;
    display: block;
    width: 100%;
    border-width: 1px;
    border-color: rgba(153, 153, 153, 0.5);
    border-style: solid;
    border-radius: 10px;
    height: 40px;
    line-height: 40px;
    &.textarea {
      height: 110px;
      resize: none;
    }
  }
  .datepicker {
    background: url(../i/cal.svg) top 10px right 12px no-repeat;
    background-size: 20px;
  }
}
/* css */
```
