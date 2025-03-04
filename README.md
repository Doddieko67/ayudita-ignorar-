# Form Automation Scripts

This repository contains JavaScript snippets for automating form filling in an Angular application. Each script targets specific form sections through ngcontent attributes.

## Table of Contents
- [Selection Helper](#selection-helper)
- [Form Elaboration](#form-elaboration)
- [Economic Information](#economic-information)
- [Housing Information](#housing-information)

## Selection Helper
Use this script to set all select elements to a specific value (in this case '3'):

```javascript
// Selects all select elements with attribute _ngcontent-mao-c93 and sets them to '3'
const selects = document.querySelectorAll('[_ngcontent-mao-c93] select');

selects.forEach(select => {
    // Set value to '3'
    select.value = '3';
    
    // Dispatch events to notify Angular about the changes
    select.dispatchEvent(new Event('change', { bubbles: true }));
    select.dispatchEvent(new Event('input', { bubbles: true }));
});
```

## Form Elaboration
Script to fill out the form elaboration section with prepopulated data:

```javascript
// Selects and fills all select elements with attribute _ngcontent-mao-c94
const selects = document.querySelectorAll('[_ngcontent-mao-c94] select');
selects.forEach(select => {
    if (select.id === 'quienElaboro') {
        select.value = '2'; // DIRECTOR REGIONAL
    } else if (select.id === 'tieneFirma') {
        select.value = '1'; // SÍ
    }
    // Trigger change event
    select.dispatchEvent(new Event('change', { bubbles: true }));
});

// Selects and fills all input elements with attribute _ngcontent-mao-c94
const inputs = document.querySelectorAll('[_ngcontent-mao-c94] input');
inputs.forEach(input => {
    if (input.id === 'idElaboro') {
        input.value = '111985';
    } else if (input.id === 'nombreElaboro') {
        input.value = 'TANIA';
    } else if (input.id === 'primerApellido') {
        input.value = 'TAPIA';
    } else if (input.id === 'segundoApellido') {
        input.value = ''; // No value provided
    }
    // Trigger input event
    input.dispatchEvent(new Event('input', { bubbles: true }));
});
```

## Economic Information
Script to fill out economic information section:

```javascript
// Selects and fills all select elements with attribute _ngcontent-mao-c88
const selects = document.querySelectorAll('[_ngcontent-mao-c88] select');
selects.forEach(select => {
    if (select.id === 'trabajaActual') {
        select.value = '0'; // NO
    } else if (select.id === 'aQueSeDedica') {
        select.value = ''; // Ignore
    } else if (select.id === 'remuneracionRecibe') {
        select.value = '0'; // NO
    } else if (select.id === 'remuneracionCuanto') {
        select.value = ''; // Ignore
    } else if (select.id === 'adicionalIngreso') {
        select.value = '1'; // SÍ
    } else if (select.id === 'adicionalOrigen') {
        select.value = '3: 3'; // PENSIÓN O PROGRAMA BIENESTAR
        select.disabled = false; // Enable if it was disabled
    } else if (select.id === 'dependeEcoAlguien') {
        select.value = '0'; // NO
    } else if (select.id === 'dependeQuien') {
        select.value = ''; // None
    } else if (select.id === 'dependeDeAlguien') {
        select.value = '0'; // NO
    } else if (select.id === 'idDependeDeAlguien') {
        select.value = ''; // Ignore
    }
    // Trigger change event
    select.dispatchEvent(new Event('change', { bubbles: true }));
});

// Selects and fills all input elements with attribute _ngcontent-mao-c88
const inputs = document.querySelectorAll('[_ngcontent-mao-c88] input');
inputs.forEach(input => {
    if (input.id === 'adicionalOrigenOtro') {
        input.value = ''; // Empty (did not select "OTRO")
    } else if (input.id === 'dependeQuienOtro') {
        input.value = ''; // Empty (did not select "OTRO")
    } else if (input.id === 'alguienDepQuienOtro') {
        input.value = ''; // Empty (did not select "OTRO")
    }
    // Trigger input event
    input.dispatchEvent(new Event('input', { bubbles: true }));
});
```

## Housing Information
Script to fill out housing information (partial due to truncation in the source):

```javascript
// Selects and fills all select elements with attribute _ngcontent-mao-c86
const selects = document.querySelectorAll('[_ngcontent-mao-c86] select');
selects.forEach(select => {
    if (select.id === 'viveendaReg') {
        select.value = '1: 1'; // PROPIA
    } else if (select.id === 'viveendaQuienesHa') {
        select.value = '1: 7'; // SOLA
    } else if (select.id === 'viveendaMatMuros') {
        select.value = '7: 7'; // TABIQUE, LADRILLO
    } else if (select.id === 'viveendaMatTecho') {
        select.value = '1: 1'; // CONCRETO
    } else if (select.id === 'viveendaMatPiso') {
        select.value = '1: 1'; // CEMENTO O FIRME
    } else if (select.id === 'cuartosVivienda') {
        select.value = '2'; // 2 CUARTOS
    }
    // Note: The original code was truncated here
    
    // Trigger change event
    select.dispatchEvent(new Event('change', { bubbles: true }));
});
```

## Usage Instructions

1. Open your browser's developer console (F12 or right-click > Inspect > Console)
2. Copy the desired script section
3. Paste into the console and press Enter to execute
4. The form fields will be automatically populated

## Notes

- All scripts dispatch the appropriate events to ensure Angular recognizes the changes
- These scripts are specific to a particular Angular application structure with specific ngcontent attributes
- Modify the ID selectors and values as needed for your specific form requirements
