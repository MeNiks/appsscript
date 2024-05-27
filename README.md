### Distance Calaulation

```javascript
function CALCULATE_DRIVING_DISTANCE(originCell, destinationCell) {

    if (!originCell || !destinationCell) {
      return "";
    }
    // originCell= \"Pune\"
    // destinationCell= \"Nanded\"
    var directions = Maps.newDirectionFinder()
        .setOrigin(originCell)
        .setDestination(destinationCell)
        .setMode(Maps.DirectionFinder.Mode.DRIVING)
        .getDirections();

    var distance = directions.routes[0].legs[0].distance.text; // .value

    // distance /= 1000; // Convert meters to kilometers
    return distance;
}

function CALCULATE_DRIVING_DURATION(originCell, destinationCell) {

    if (!originCell || !destinationCell) {
      return "";
    }
    // originCell= \"Pune\"
    // destinationCell= \"Nanded\"
    var directions = Maps.newDirectionFinder()
        .setOrigin(originCell)
        .setDestination(destinationCell)
        .setMode(Maps.DirectionFinder.Mode.DRIVING)
        .getDirections();
    return directions.routes[0].legs[0].duration.text
}

```
