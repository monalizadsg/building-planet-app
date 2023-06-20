# :earth_americas: building-planet-app
 An app that displays list of planets with information. User will be able to delete a planet.
 
 An exercise to practice building react components.

## :arrow_down: Tasks
:white_check_mark: Create a planet card that accept props and to be rendered when planet array is iterated.

   - use `destructuring` to get the values of props and directly call it in the component.
   ```js
    const { id, name, diameter, moons, desc, url, removePlanet } = props;
      
      <div>
        <img src={url} alt={name} />
      </div>
      <h2>{name}</h2>
      <p>{desc}</p>
      ...
   ```
   - use `spread operator` to pass all the properties of planet obj to planet card.
   ```js
   <div className='container'>
        {this.state.planets.map((planet) => (
          <PlanetCard
            key={planet.id}
            {...planet}
            removePlanet={this.handleRemovePlanet}
          />
        ))}
   </div>
   ```
   

:white_check_mark: Add a delete btn so user can remove a planet.

  - x button is shown when user hovered the card.
    
  - when x button is clicked, planet will be removed from the list and the app will be re-rendered.
    
  - .filter() is used to removed the selected item from the list.
