A fully-featured and customizable Modal component for React, with support for title, content, and custom actions.

## Installation
`npm install agr-custom-modal`

## Usage

In this example, the Modal component is used to display a simple modal dialog when a button is clicked. The isOpen prop is used to control whether the modal is displayed or hidden, and the onClose prop is used to handle the closing of the modal. The title and content of the modal are passed as children to the component.

```react
import React, { useState } from 'react';
import Modal from 'agr-custom-modal';

function App() {
  const [showModal, setShowModal] = useState(false);

  const handleOpenModal = () => {
    setShowModal(true);
  };

  const handleCloseModal = () => {
    setShowModal(false);
  };

  return (
    <div>
      <button onClick={handleOpenModal}>Open Modal</button>
      <Modal
        title="Example Modal"
        isOpen={showModal}
        onClose={handleCloseModal}
      >
        <p>This is the body of the modal.</p>
        <button onClick={handleCloseModal}>Close Modal</button>
      </Modal>
    </div>
  );
}

export default App;
```

## Props

| Prop  | Type  | Required | Description
| :------------ |:---------------:| -----:| ------------:|
| title      | string | Yes | The title of the Modal
| isOpen      | boolean        |   Yes | Determines whether the Modal is visible or not
| onClose | function        |    Yes | Callback function that is called when the Modal is closed
| children | node        |    No | The content of the Modal
----

## Customization
The Modal component can be easily customized by modifying the CSS styles that are applied to it. The component is designed to be as unobtrusive as possible, with a minimal set of default styles that can be easily overridden.

To customize the styles of the Modal component, you can create a new CSS file and import it into your application:

```css
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 9999;
}

.modal-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: white;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}

.modal-header h2 {
  margin: 0;
  font-size: 1.5rem;
}

.close-button {
  background-color: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
}
```

In this example, the default styles for the Modal component

## Contributing

If you'd like to contribute to this project, please submit a pull request or create an issue on the Github repository.

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for details.# react-custom-modal
