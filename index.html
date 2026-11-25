const display = document.getElementById("display");
const previous = document.getElementById("previous");

const calculator = document.getElementById("calculator");
const gameCenter = document.getElementById("game-center");
const backButton = document.getElementById("back-button");


/* =================================
   SECRET CODE
   PUT YOUR SECRET CODE BELOW
================================= */

const SECRET_CODE = "6767";


/* CALCULATOR VARIABLES */

let current = "0";
let stored = null;
let operation = null;
let resetNext = false;


function update() {
    display.textContent = current;
}


function calculate(a, b, op) {
    switch (op) {
        case "+":
            return a + b;

        case "−":
            return a - b;

        case "×":
            return a * b;

        case "÷":
            return b === 0 ? null : a / b;

        default:
            return b;
    }
}


function format(number) {
    if (!Number.isFinite(number)) return "Error";

    return String(Number(number.toPrecision(10)));
}


function enter(value) {
    if (resetNext) {
        current = value === "." ? "0." : value;
        resetNext = false;

    } else if (value === ".") {
        if (!current.includes(".")) {
            current += ".";
        }

    } else {
        current = current === "0" ? value : current + value;
    }

    update();
}


/* =================================
   GAME CENTER
================================= */

function openGameCenter() {
    calculator.hidden = true;
    gameCenter.hidden = false;
}


function closeGameCenter() {
    gameCenter.hidden = true;
    calculator.hidden = false;

    clear();
}


/* =================================
   CALCULATOR OPERATIONS
================================= */

function chooseOperator(op) {
    const value = Number(current);

    if (operation && stored !== null && !resetNext) {
        const result = calculate(stored, value, operation);

        if (result === null) {
            current = "Error";
            stored = null;
            operation = null;
            previous.textContent = "";
            resetNext = true;

            update();
            return;
        }

        current = format(result);
    }

    stored = Number(current);
    operation = op;

    previous.textContent = `${current} ${op}`;

    resetNext = true;

    update();
}


function equals() {

    // Check secret code before normal calculation.
    if (
        operation === null &&
        stored === null &&
        SECRET_CODE !== "PUT_YOUR_SECRET_CODE_HERE" &&
        current === SECRET_CODE
    ) {
        openGameCenter();
        return;
    }

    // Normal calculator functionality.
    if (operation === null || stored === null) return;

    const result = calculate(
        stored,
        Number(current),
        operation
    );

    previous.textContent =
        `${stored} ${operation} ${current} =`;

    current = result === null ? "Error" : format(result);

    stored = null;
    operation = null;
    resetNext = true;

    update();
}


function clear() {
    current = "0";
    stored = null;
    operation = null;
    resetNext = false;

    previous.textContent = "";

    update();
}


/* =================================
   BUTTON CONTROLS
================================= */

document.querySelector(".buttons").addEventListener("click", event => {

    const button = event.target.closest("button");

    if (!button) return;

    const action = button.dataset.action;
    const value = button.dataset.value;

    if (action === "clear") {
        clear();
    }

    else if (action === "delete") {

        if (resetNext || current === "Error") {
            current = "0";
            resetNext = false;

        } else {
            current = current.length > 1
                ? current.slice(0, -1)
                : "0";
        }

        update();
    }

    else if (action === "sign") {

        if (current !== "0" && current !== "Error") {
            current = String(-Number(current));
            update();
        }
    }

    else if (action === "percent") {

        if (current !== "Error") {
            current = format(Number(current) / 100);
            update();
        }
    }

    else if (action === "operator") {
        chooseOperator(value);
    }

    else if (action === "equals") {
        equals();
    }

    else if (value !== undefined) {
        enter(value);
    }

});


/* =================================
   KEYBOARD CONTROLS
================================= */

document.addEventListener("keydown", event => {

    // Don't interfere with Game Center.
    if (!gameCenter.hidden) return;

    if (/^[0-9.]$/.test(event.key)) {
        enter(event.key);
    }

    else if (event.key === "+") {
        chooseOperator("+");
    }

    else if (event.key === "-") {
        chooseOperator("−");
    }

    else if (event.key === "*") {
        chooseOperator("×");
    }

    else if (event.key === "/") {
        event.preventDefault();
        chooseOperator("÷");
    }

    else if (event.key === "Enter" || event.key === "=") {
        event.preventDefault();
        equals();
    }

    else if (event.key === "Backspace") {

        if (resetNext || current === "Error") {
            current = "0";
            resetNext = false;

        } else {
            current = current.length > 1
                ? current.slice(0, -1)
                : "0";
        }

        update();
    }

    else if (event.key === "Escape") {
        clear();
    }

});


/* =================================
   BACK BUTTON
================================= */

backButton.addEventListener("click", closeGameCenter);


// Initialize calculator
update();
