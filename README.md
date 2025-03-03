# TODOS

[TODOS LINK](http://127.0.0.1:4700 "The best for automated testing of todo lists!").

(czy po 4700 powinna być wersja aplikacji?)

This project serves the purpose of creating todo lists that can be later edited to show the overall progress of one's planned activities.

3. New Todo
    - Should allow me to add todo items
    - adds items



1. Checking if the "Clear completed" button will disappear if we edit ticked todo with spaces/Sprawdzenie czy przycisk "Clear completed" zniknie jeśli edytujemy zaznaczone todo samymi spacjami
- should allow me to make the "Clear completed" button disappear 
- button disappears when todo is edited with spaces

2. Sprawdzenie czy możliwe jest przełączanie się między nowo dodanymi todo oraz elementami aplikacji za pomocą klawisza Tab i Shift + Tab
- 


3. Sprawdzenie czy możliwe jest wklejenie obrazu do pola tekstowego
- 


4. Sprawdzenie czy input pola tekstowego podlega sanityzacji
- 


let fixture = {
  "fixtures": {
    "idOneExtra": {
      "fiveSpaces": "     ",
      "tenSpacesOverLimit": "          ",
      "minNumberOfSpaces": " ",
      "tabsOnly": "\t\t\t",
      "newLinesOnly": "\n\n\n",
      "mixedWhitespaceCheck": "\t \t \t",
      "newlineAndSpaceCombination": "\r\n \n \r",
      "regularAndNonBreakingSpaces": " \u00A0 ",
      "verticalTabulators": "\v\v\v",
      "wideSpacesEmSpace": "\u2003\u2003\u2003",
      "zeroWidthSpaces": "\u200B\u200B\u200B",
      "nonBreakingSpacesNbsp": "\xA0\xA0\xA0",
      "fullWidthSpacesChineseJapanese": "\u3000\u3000\u3000",
      "mediumMathematicalSpaces": "\u205F\u205F\u205F",
      "tabNewlineSpaceInvisibleChars": "\t \n \r \xA0\u200B",
      "singleSpaceWithZeroWidth": " \u200B ",
      "tabsAndNewlinesNoContent": "\t\n\t\n"
    },
    "idFourExtra": {
      "normalLink": "https://example.com",
      "maliciousLink": "<script>alert('Hacked!')</script>",
      "htmlInjection": "<b>Bold Text</b>",
      "sqlInjection": "' OR '1'='1'; --",
      "javaScriptInjection": "javascript:alert('XSS')",
      "eventHandlerInjection": "<img src=x onerror=alert(1)>",
      "obfuscationJavaScript": "<ScRiPt>alert('XSS')</sCrIpT>",
      "cssInjection": "<style>body {background: red;}</style>",
      "controlCharactersAscii": "\x00\x1F\x7F",
      "linkScriptCombination": "http://evil.com\" onmouseover=\"alert('Hacked!')\"",
      "svgInjection": "<svg><script>alert('XSS')</script></svg>",
      "nestedInjection": "<div><script>alert('XSS')</script></div>",
      "doubleEncodingXss": "%3Cscript%3Ealert('XSS')%3C/script%3E",
      "domBasedXss": "<input onfocus=alert(1)>"
    }
  }
}
