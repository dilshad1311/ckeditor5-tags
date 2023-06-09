# ckeditor5-tags

## Install

```bash
npm install --save  ckeditor5-tags
```

## Usage

```jsx
import React, { Component } from 'react'

import {CKEditor} from '@ckeditor/ckeditor5-react';
import Editor from 'ckeditor5-tags';

const TextEditor = ({value, onChange, label, required, disabled, error, tags, readOnly}) => {

  return (
    <div className={`ckeditor-container ${error ? 'with-error' : ''}`}>
      <CKEditor
        editor={Editor}
        config={{label, tags, required, readOnly, disabled}}
        data={value}
        onReady={editor => {
          if (readOnly || disabled)
            editor.isReadOnly = true
        }}
        onChange={(event, editor) => {
          onChange(editor.getData());
        }}
      />
    </div>
  );
};
```

## Screenshot



