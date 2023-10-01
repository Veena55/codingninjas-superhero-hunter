# codingninjas-superhero-hunter
Coding Ninjas SuperHero Hunter

# Created json file by extracting results array from all 16 elements.
 window.onload = async()=> {
            const response = await fetch('./response.json')
            const result = await response.json(); 
            var allCharacters = [];
            for (const key in result) {
                if (Object.hasOwnProperty.call(result, key)) {
                    const element = result[key].data.results;   
                    allCharacters = [...allCharacters, ...element];                 
                }
            }
            console.log(allCharacters);            
        }
# Functionalities
--loadHomePage -  Fetch all marvel charcters on homepage.
--refreshFavourities - Cookies get refreshed for favourites foreach request.
--addCard - add cards dynamically as per the request.
--toggleFavourite - add or remove favourites.
--loadFavouriteCharacters - loading the list of all favourite characters.
--showSuperHeroDetails - showing the full detail on cliking the particular character.