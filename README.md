# 🍰 CakeUI Editor

> Markdown (GFM) + WYSIWYG Editor — Fork of [Toast UI Editor](https://github.com/nhn/tui.editor)

CakeUI is a **fork of Toast UI Editor**, customized for personal projects while keeping the original’s productivity and extensibility. This fork is maintained independently and can be used as a lightweight, flexible Markdown/WYSIWYG editor.

---

## 📦 Packages

| Package | Description |
| ------- | ----------- |
| `cakeui.editor` | Plain JavaScript editor component |
| `cakeui.react-editor` | React wrapper |
| `cakeui.vue-editor` | Vue wrapper |

Optional plugins include: charts, syntax highlighting, color styling, table merges, and UML diagrams.

---

## ⚡ Features

- Markdown + WYSIWYG modes  
- Live preview & scroll sync  
- Toolbar & formatting controls  
- Dark theme support  
- Plugins for charts, UML, code highlighting, color syntax, and table merges  

---

## 🐾 Usage

Include `dist` files directly in your project:

    
    <link rel="stylesheet" href="dist/cakeui-editor.min.css" />
    <script src="dist/cakeui-editor.min.js"></script>
    
    <div id="editor"></div>
    <script>
      const editor = new CakeUI.Editor({
        el: document.getElementById('editor'),
        initialEditType: 'markdown',
        previewStyle: 'vertical',
        height: '400px'
      });
    </script>


---

## 🔧 Development (master branch)

      git clone -b master https://github.com/surajtechsmith/cakeui.editor.git
      cd cakeui.editor
      npm install
      npm run build


---

## 📜 License
    
MIT License — forked from [Toast UI Editor](https://github.com/nhn/tui.editor)
Maintained independently as **CakeUI Editor**.
    
    
