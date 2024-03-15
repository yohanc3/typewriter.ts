# Typewriter React Hook

Typewriter effect for React + TS

Iterates through the given array of string and returns each element letter by letter with a given/default interval (default is 50ms). Time interval at the end of each element and the beggining of the next one can also be passed, if not, it is set to a default 2000ms.  

## Install

```
npm i typewriter-hook
```

## How to use
``` TypeScript
import { useTypewriter } from "typewriter-hook"

export default function HelloWorld(){
    
    const PHRASES = [
        "top 3 movies of all time",
        "fastest land animal",
        "beethoven"
    ]
    
    //optional, default values are 50 and 2000.
    const LETTER_INTERVAL = 50;
    const WORD_INTERVAL = 2000;
    
    const [ text ] = useTypewriter(PHRASES, LETTER_INTERVAL, WORD_INTERVAL )
    
    return (
        <main className="text-5xl flex items-center justify-center"> 
            { text }
        <main/>
    )
    
}
```

## Result
https://github.com/yohanc3/typewriter.ts/assets/116668883/3f8e8824-b981-466f-846d-c3420f6364cc



## Parameters

- PHRASES: Array of strings
- LETTER_INTERVAL: Interval between the concatenation of each letter
- WORD_INTERVAL: Interval between the end of each string and the beginning of the next one
