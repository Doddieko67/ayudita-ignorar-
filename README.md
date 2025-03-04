## TODO EN UNO SOLOOO :))))
```javascript
// Paso 1: Llenar "Ocupación e Ingreso" (_ngcontent-mao-c88)
setTimeout(() => {
    const selectsC88 = document.querySelectorAll('[_ngcontent-mao-c88] select');
    selectsC88.forEach(select => {
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
        select.dispatchEvent(new Event('change', { bubbles: true }));
    });

    const inputsC88 = document.querySelectorAll('[_ngcontent-mao-c88] input');
    inputsC88.forEach(input => {
        if (input.id === 'adicionalOrigenOtro') {
            input.value = ''; // Empty
        } else if (input.id === 'dependeQuienOtro') {
            input.value = ''; // Empty
        } else if (input.id === 'alguienDepQuienOtro') {
            input.value = ''; // Empty
        }
        input.dispatchEvent(new Event('input', { bubbles: true }));
    });

    // Paso 2: Llenar todos los selects con '3' (_ngcontent-mao-c93)
    setTimeout(() => {
        const selectsC93 = document.querySelectorAll('[_ngcontent-mao-c93] select');
        selectsC93.forEach(select => {
            select.value = '3';
            select.dispatchEvent(new Event('change', { bubbles: true }));
            select.dispatchEvent(new Event('input', { bubbles: true }));
        });

        // Paso 3: Llenar "Vivienda" (_ngcontent-mao-c86)
        setTimeout(() => {
            const selectsC86 = document.querySelectorAll('[_ngcontent-mao-c86] select');
            selectsC86.forEach(select => {
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
                select.dispatchEvent(new Event('change', { bubbles: true }));
            });

            // Paso 4: Marcar solo "MANUALIDADES" (_ngcontent-mao-c90)
            setTimeout(() => {
                const inputsC90 = document.querySelectorAll('[_ngcontent-mao-c90] input');
                inputsC90.forEach(input => {
                    if (input.type === 'checkbox') {
                        if (input.id === 'manualidades') {
                            input.checked = true;
                        } else {
                            input.checked = false; // Ignorar el resto
                        }
                        input.dispatchEvent(new Event('change', { bubbles: true }));
                        input.dispatchEvent(new Event('input', { bubbles: true }));
                    } else if (input.type === 'text') {
                        if (input.id === 'actividadRealizarOtro1' || 
                            input.id === 'actividadRealizarOtro2' || 
                            input.id === 'actividadRealizarOtro3') {
                            input.value = '';
                            input.dispatchEvent(new Event('input', { bubbles: true }));
                            input.dispatchEvent(new Event('change', { bubbles: true }));
                        }
                    }
                });

                const siguienteBtn1 = document.querySelector('.btn-siguiente');
                if (siguienteBtn1) siguienteBtn1.click();

                // Paso 5: Seleccionar "NO" en "VIOLENCIA Y DISCRIMINACIÓN" (_ngcontent-mao-c91)
                setTimeout(() => {
                    const selectsC91 = document.querySelectorAll('[_ngcontent-mao-c91] select');
                    selectsC91.forEach(select => {
                        if (select.id === 'situacionViolencia') {
                            select.value = '0'; // NO
                            select.dispatchEvent(new Event('change', { bubbles: true }));
                            select.dispatchEvent(new Event('input', { bubbles: true }));
                        }
                    });

                    const siguienteBtn2 = document.querySelector('.btn-siguiente');
                    if (siguienteBtn2) siguienteBtn2.click();

                    // Paso 6: Seleccionar "NO" en "OBSERVACIONES" (_ngcontent-mao-c92)
                    setTimeout(() => {
                        const selectsC92 = document.querySelectorAll('[_ngcontent-mao-c92] select');
                        selectsC92.forEach(select => {
                            if (select.id === 'tieneObser') {
                                select.value = '0'; // NO
                                select.dispatchEvent(new Event('change', { bubbles: true }));
                                select.dispatchEvent(new Event('input', { bubbles: true }));
                            }
                        });

                        const inputsC92 = document.querySelectorAll('[_ngcontent-mao-c92] input');
                        inputsC92.forEach(input => {
                            if (input.id === 'oBservaciones') {
                                input.value = ''; // Vacío porque es "NO"
                                input.dispatchEvent(new Event('input', { bubbles: true }));
                                input.dispatchEvent(new Event('change', { bubbles: true }));
                            }
                        });

                        const siguienteBtn3 = document.querySelector('.btn-siguiente');
                        if (siguienteBtn3) siguienteBtn3.click();

                        // Paso 7: Llenar "ELABORACIÓN" (_ngcontent-mao-c94)
                        setTimeout(() => {
                            const selectsC94 = document.querySelectorAll('[_ngcontent-mao-c94] select');
                            selectsC94.forEach(select => {
                                if (select.id === 'quienElaboro') {
                                    select.value = '2'; // DIRECTOR REGIONAL
                                } else if (select.id === 'tieneFirma') {
                                    select.value = '1'; // SÍ
                                }
                                select.dispatchEvent(new Event('change', { bubbles: true }));
                            });

                            const inputsC94 = document.querySelectorAll('[_ngcontent-mao-c94] input');
                            inputsC94.forEach(input => {
                                if (input.id === 'idElaboro') {
                                    input.value = '111985';
                                } else if (input.id === 'nombreElaboro') {
                                    input.value = 'TANIA';
                                } else if (input.id === 'primerApellido') {
                                    input.value = 'TAPIA';
                                } else if (input.id === 'segundoApellido') {
                                    input.value = '';
                                }
                                input.dispatchEvent(new Event('input', { bubbles: true }));
                            });
                        }, 300); // Paso 7: 300ms después de Observaciones
                    }, 300); // Paso 6: 300ms después de Violencia
                }, 300); // Paso 5: 300ms después de Actividades
            }, 300); // Paso 4: 300ms después de Vivienda
        }, 300); // Paso 3: 300ms después de C93
    }, 300); // Paso 2: 300ms después de C88
}, 300); // Paso 1: Comienza después de 300ms
```

## Coacalco 
```javascript
// Seleccionar todos los <ng-select> con el atributo [_ngcontent-mao-c84]
const ngSelects = document.querySelectorAll('[_ngcontent-mao-c84] ng-select');
ngSelects.forEach(ngSelect => {
    const input = ngSelect.querySelector('input'); // El input interno del ng-select

    if (ngSelect.id === 'municipio') {
        if (input) {
            input.value = '15020 - COACALCO DE BERRIOZABAL';
        }
    } else if (ngSelect.id === 'localidad') {
        if (input) {
            input.value = '150200001 - SAN FRANCISCO COACALCO';
        }
    } else if (ngSelect.id === 'colonia') {
        if (input) {
            input.value = '5002000792 - UNIDAD HABITACIONAL SAN RAFAEL';
        }
    }
    input.dispatchEvent(new Event('change', { bubbles: true }));
    input.dispatchEvent(new Event('input', { bubbles: true }));
});
```


## Economic Information

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

## Todos solitos :(

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

## La viviendaaaaa

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

## Ocio, violencia, observacion y Taniaaaa tapiaaa
Script to fill out the form elaboration section with prepopulated data:

```javascript
// Paso 1: Marcar solo "MANUALIDADES" en el formulario de actividades (_ngcontent-mao-c90)
const inputsC90 = document.querySelectorAll('[_ngcontent-mao-c90] input');
inputsC90.forEach(input => {
    if (input.type === 'checkbox') {
        if (input.id === 'manualidades') {
            input.checked = true;
        } else {
            input.checked = false; // Ignorar el resto
        }
        input.dispatchEvent(new Event('change', { bubbles: true }));
        input.dispatchEvent(new Event('input', { bubbles: true }));
    } else if (input.type === 'text') {
        if (input.id === 'actividadRealizarOtro1' || 
            input.id === 'actividadRealizarOtro2' || 
            input.id === 'actividadRealizarOtro3') {
            input.value = '';
            input.dispatchEvent(new Event('input', { bubbles: true }));
            input.dispatchEvent(new Event('change', { bubbles: true }));
        }
    }
});

// Simular clic en el botón "Siguiente" después de 1 segundo (ajusta el tiempo si necesitas)
setTimeout(() => {
    const siguienteBtn1 = document.querySelector('.btn-siguiente'); // Asumiendo una clase genérica
    if (siguienteBtn1) siguienteBtn1.click();

    // Paso 2: Seleccionar "NO" en "VIOLENCIA Y DISCRIMINACIÓN" (_ngcontent-mao-c91)
    const selectsC91 = document.querySelectorAll('[_ngcontent-mao-c91] select');
    selectsC91.forEach(select => {
        if (select.id === 'situacionViolencia') {
            select.value = '0'; // NO
            select.dispatchEvent(new Event('change', { bubbles: true }));
            select.dispatchEvent(new Event('input', { bubbles: true }));
        }
    });

    // Simular clic en el botón "Siguiente" después de otro segundo
    setTimeout(() => {
        const siguienteBtn2 = document.querySelector('.btn-siguiente');
        if (siguienteBtn2) siguienteBtn2.click();

        // Paso 3: Seleccionar "NO" en "OBSERVACIONES" (_ngcontent-mao-c92)
        const selectsC92 = document.querySelectorAll('[_ngcontent-mao-c92] select');
        selectsC92.forEach(select => {
            if (select.id === 'tieneObser') {
                select.value = '0'; // NO
                select.dispatchEvent(new Event('change', { bubbles: true }));
                select.dispatchEvent(new Event('input', { bubbles: true }));
            }
        });

        const inputsC92 = document.querySelectorAll('[_ngcontent-mao-c92] input');
        inputsC92.forEach(input => {
            if (input.id === 'oBservaciones') {
                input.value = ''; // Vacío porque es "NO"
                input.dispatchEvent(new Event('input', { bubbles: true }));
                input.dispatchEvent(new Event('change', { bubbles: true }));
            }
        });

        // Simular clic en el botón "Siguiente" después de otro segundo
        setTimeout(() => {
            const siguienteBtn3 = document.querySelector('.btn-siguiente');
            if (siguienteBtn3) siguienteBtn3.click();

            // Paso 4: Llenar "ELABORACIÓN" (_ngcontent-mao-c94)
            const selectsC94 = document.querySelectorAll('[_ngcontent-mao-c94] select');
            selectsC94.forEach(select => {
                if (select.id === 'quienElaboro') {
                    select.value = '2'; // DIRECTOR REGIONAL
                } else if (select.id === 'tieneFirma') {
                    select.value = '1'; // SÍ
                }
                select.dispatchEvent(new Event('change', { bubbles: true }));
            });

            const inputsC94 = document.querySelectorAll('[_ngcontent-mao-c94] input');
            inputsC94.forEach(input => {
                if (input.id === 'idElaboro') {
                    input.value = '111985';
                } else if (input.id === 'nombreElaboro') {
                    input.value = 'TANIA';
                } else if (input.id === 'primerApellido') {
                    input.value = 'TAPIA';
                } else if (input.id === 'segundoApellido') {
                    input.value = '';
                }
                input.dispatchEvent(new Event('input', { bubbles: true }));
            });
        }, 1000); // Tiempo antes de ir al formulario de elaboración
    }, 1000); // Tiempo antes de ir al formulario de observaciones
}, 1000); // Tiempo antes de ir al formulario de violencia
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
