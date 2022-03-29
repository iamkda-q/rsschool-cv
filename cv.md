# Dmitriy Konnov
----------
### Contacts:
- **Discord:** Dimas#0904
- **E-mail:** iamkda@mail.ru
- **Tel:** +7-999-___-__-__

### About myself:
I started studying web development in September 2021 with the Yandex Practicum program. I want to try my hand at web development, because I'm a little tired of the monotony in my current profession.

### Projects with HTML/CSS/JS/React:
*You can look at my github https://github.com/iamkda-q*

### Work experience:
*Have no commercial experience as a web-developer.*

### Education and courses:
1. JavaScript https://learn.javascript.ru/
2. Yandex Practicum Web-developer https://practicum.yandex.ru/profile/web/
3. Codewars https://www.codewars.com/users/iamkda-q
4. RS School JS/Frontend Stage 0 (partly) https://rs.school/js-stage0/

### Language:
English - At the level of reading technical documentation.


### Code example:
```javascript
function convert(input, source, target) {
    const sLn = source.length;
    const tLn = target.length;
    if (input == "0") return target[0];
    function transformToTarget(input, numbSystLength) {
        const res = [];
        while (input > 0) {
            res.push(input % numbSystLength);
            input = Math.floor(input / numbSystLength);
        }
        return res
    }
    function transformToDecimal(input, sLn) {
        return input.reduce((dec, item, i) => {
            return dec += item * Math.pow(sLn, input.length - 1 - i);
        }, 0)
    }
    function transformFromNumberic(mas) {
        return mas.reverse().map(item => target[item]).join("");
    }

    function transformToNumberic(input) {
        debugger;
        return input.split("").map(item => source.indexOf(item));
    }
    return transformFromNumberic(transformToTarget(transformToDecimal(transformToNumberic(input), sLn), tLn));
}

var Alphabet = {
    BINARY: "01",
    OCTAL: "01234567",
    DECIMAL: "0123456789",
    HEXA_DECIMAL: "0123456789abcdef",
    ALPHA_LOWER: "abcdefghijklmnopqrstuvwxyz",
    ALPHA_UPPER: "ABCDEFGHIJKLMNOPQRSTUVWXYZ",
    ALPHA: "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ",
    ALPHA_NUMERIC:
        "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ",
        aa: "abcdefghijkl",
};


// convert between numeral systems
console.log(convert("15", Alphabet.DECIMAL, Alphabet.BINARY)); // should return "1111"
console.log(convert("15", Alphabet.DECIMAL, Alphabet.OCTAL)); // should return "17"
console.log(convert("1010", Alphabet.BINARY, Alphabet.DECIMAL)); // should return "10"
console.log(convert("1010", Alphabet.BINARY, Alphabet.HEXA_DECIMAL)); // should return "a"

// // other bases
console.log(convert("0", Alphabet.DECIMAL, Alphabet.ALPHA)); // should return "a"
console.log(convert("27", Alphabet.DECIMAL, Alphabet.ALPHA_LOWER)); // should return "bb"
console.log(convert("hello", Alphabet.ALPHA_LOWER, Alphabet.HEXA_DECIMAL)); // should return "320048"
console.log(convert("SAME", Alphabet.ALPHA_UPPER, Alphabet.ALPHA_UPPER)); // should return "SAME"
console.log(convert("2322", Alphabet.OCTAL, Alphabet.HEXA_DECIMAL)); // should return "4D2"
console.log(convert("4d2", Alphabet.HEXA_DECIMAL, Alphabet.OCTAL)); // should return "2322"
```
