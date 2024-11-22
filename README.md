# Pokemon.random
function generateRandomNumber(num) {
    return Math.floor(Math.random() * num);
}

const myTeam = {
    pokemons: ['Gyarados', 'Snorlax', 'Pikachu', 'Vaporeon'],
    pokemonStatus: ['confused!', 'poisoned!','Freeze!','K.O!'],
    advice: ['use this Berry!', 'use this Potion!', 'use the nearest pokemon centre!','use Full restore!']

}
let myOption = []
for (let prop in myTeam) {
    let optionIdx = generateRandomNumber(myTeam[prop].length)
    switch (prop) {
        case 'pokemons':
            myOption.push(`Your "${myTeam[prop][optionIdx]}".`)
            break
            case 'pokemonStatus':
                myOption.push(`Has Been "${myTeam[prop][optionIdx]}".`)
                break
                case 'advice':
                    myOption.push(`Quick "${myTeam[prop][optionIdx]}".`)
                    
    }
}
console.log(myOption);
