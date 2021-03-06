# React Marky Markdown
[![npm version](https://badge.fury.io/js/react-marky-markdown.svg)](https://badge.fury.io/js/react-marky-markdown)

A clean markdown editor for react.

Currently in beta. Like this readme :)

## Usage

`yarn add react-marky-markdown`

```js
import { Editor, Mention } from 'react-marky-markdown';
// Includes necessary styling
import 'react-marky-markdown/dist/styles.css';

const App = () => {
  return (
    <Editor>
      <Mention
        prefix="@"
        data={[
          { value: 'terminator', label: 'Arnold Schwarzenegger' },
          { value: 'markymark', label: 'Mark wahlberg' },
        ]}
      />
    </Editor>
  );
};
```

## Props

```ts
// Editor
{
  defaultValue?: string;
  onChange?(value: string): void;
  onSubmit?(): void;
  onBlur?(): void;
  onCancel?(): void;
}

// Mention
{
  prefix: string;
  data: MentionData[]; // { value: string | number; label: string; }
  onSearch?(value: string): void;
}
```