```js
App.js

import { Grid, list } from "@chakra-ui/react";

import { useState } from "react";

import "./App.css";

import { Way } from "./components/Way";

  

// these are object of key valuee pairs and they reffered to state

let initial = {

  question1: "",

  question2: "",

  question3: "sample 3",

};

  

// const array = ["1way", "2way", "3way", "4way", "5way"];

  

function App() {

  // these are above mentioned object and it was set as the state for the reused way components

  const [state, setState] = useState({

    "1way": initial,

    "2way": initial,

    "3way": initial,

    "4way": initial,

    "5way": initial,

  });

  // const [array, SetArray] = useState([]);

  

  return (

    <Grid gap={8}>

      {/* one onChange but it has the properties of question 1,question 2, question 3 //the question is sent as props to App.js So it works for question1,2,3// */}

      <Way

        //tittle is reffered to the App.js

  

        title={"1 ways"}

        value={state["1way"]}

        onChange={(question, value) => {

          console.log(question);

          setState({

            ...state,

            "1way": {

              ...state["1way"],

              [question]: value,

            },

          });

        }}

      />

      {/* <Way title={"2 ways"} onChange={(value) => {}} />

      <Way title={"3 ways"} onChange={(value) => {}} />

      <Way title={"4 ways"} onChange={(value) => {}} />

      <Way title={"5 ways"} onChange={(value) => {}} /> */}

    </Grid>

  );

}

  

export default App;
```

```js
Way.js

import { Grid, Text } from '@chakra-ui/react'

import { CustomInput } from './ui/Input'

  

//  this are props of App.js

export function Way({ title, value, onChange }) {

    return (

        <Grid gridTemplateColumns={' 50px 1fr  1fr 1fr 1fr'} columnGap={5}>

            <Text >{title}</Text>

            {/* this question1 ,2,3 are indicicating the input boxes i.e CustomInput */}

            <CustomInput value={value.question1} onChange={(e) => onChange("question1", e.target.value)} />

            <CustomInput value={value.question2} onChange={(e) => onChange("question2", e.target.value)} />

            <CustomInput value={value.question3} onChange={(e) => onChange("question3", e.target.value)} />

        </Grid>

    )

}
```

``` js
input.jsx

import { Input } from "@chakra-ui/react";

import React from "react";

  

// way.jsx oda onChange and value

export const CustomInput = ({ value, onChange }) => (

  <Input

    width="auto"

    height="150px"

    border="3px  solid"

    value={value}

    onChange={onChange}

  />

);

```