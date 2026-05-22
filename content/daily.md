+++
title = "Daily"
+++

## Timothy C. May - The Crypto Anarchist Manifesto

And just as a seemingly minor invention like barbed wire made possible the fencing-off of vast ranches and farms, thus altering forever the concepts of land and property rights in the frontier West, so too will the seemingly minor discovery out of an arcane branch of mathematics come to be the wire clippers which dismantle the barbed wire around intellectual property.

*Arise, you have nothing to lose but your barbed wire fences!*

## GPG Terminal Commands  
[gpg-key commands](/gpg-keys/)

## How Miners Work ?
Imagine 64-digit Hexadecimal number. This is the output of SHA256 hash function!  
example:  
`hello world! -> 7509e5bda0c762d2bac7f90d758b5b2263fa01ccbc542ab5e3df163be08e6ca9`  
so basically SHA256 can create a 64-digit SPECIFIC RANDOM HEXADECIMAL NUMBER from any string.  
You can change the whole number with small changes in your string:   
`Hello world! -> c0535e4be2b79ffd93291305436bf889314e4a3faec05ecffcbb7df31ad9e51a`  
 now imagine there is a game and the rule is that to find a number which is smaller or equal to:  
`00000000000000000f9924b017a48ef8b16311e0a2e6fa9f3f1822bc05cc197` (look at it like `0034` in decimal)    
This is **Target**.   
All of the transactions updated in MEMPOOL. (https://mempool.space) Miners select transactions from mempool based on the higher fees.  
after this , Miner try to hash all the transactions information (sender address , receiver address , amount , date and etc. ) with a decimal number (starts from 0 , we call it NONCE )
to find a hex value, equal or smaller than TARGET value.  
The zeros of the Target value called **difficulty**. Bitcoin Protocol can update it by current miners activity and hash rate. 

## How Miners Work? 2
You can simulate how real miners work in Hard-Mode: https://bitpolito-mining-game.vercel.app  
I made it btw... hahaha
Created with Love by BitPolito

## Fun fact #1  
if you don't know a single shit about how to program, It doesn't matter.  
but if you don't know how a program should work , kill yourself. 
coding does NOT matter anymore.  
BASIC KNOWLEDGES STILL ON TOP...

## Am I wrong?  
Tonight, after a long time, maybe I've reached the point where I can admit that I made a mistake for 4 years. 

## 23May2026  
I spent 20 days for developing a web app. 
trying different algorithms and solutions to find the best way to simulate BTC miners.(and research to see how it really works and how can I similate it in the simplest way.) tomorrow morning it will be presented...  
I'm not there. I hope it works :)💙

