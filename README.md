# Project Name
> mysteriousOrganism

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Code Examples](#code-examples)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info
A sorting function using arrays to determine surviving specimen

## Technologies
* JavaScript
* Git/GitHub  

## Setup
Runs thru console 

## Code Examples
Show examples of usage:
`const pAequorFactory = (specimanNum, dna) => {
    return {
      specimanNum,
      dna,
      mutate() {
        const randIndex = Math.floor(Math.random() * this.dna.length);
        let newBase = returnRandBase();
        while (this.dna[randIndex] === newBase) {
          newBase = returnRandBase();
        }
        this.dna[randIndex] = newBase;
        return this.dna;
      },
      compareDNA(otherOrg) {
        const similarities = this.dna.reduce((acc, curr, idx, arr) => {
          if (arr[idx] === otherOrg.dna[idx]) {
            return acc + 1;
          } else {
            return acc;
          }
        }, 0);
        const percentOfDNAshared = (similarities / this.dna.length) * 100;
        const percentageTo2Deci = percentOfDNAshared.toFixed(2);
        console.log(`${this.specimanNum} and ${otherOrg.specimanNum} have ${percentageTo2Deci}% DNA in common.`);
      },
      willLikelySurvive() {
        const cOrG = this.dna.filter(el => el === "C" || el === "G");
        return cOrG.length / this.dna.length >= 0.6;
      },
    }
  };`

## Status
Project is: _finished_

## Inspiration
Created with Codecademy's Full Stack Engineer pathway 

## Contact
Created by TarrMarr(https://www.tarrynmarr.me) - feel free to contact me!
