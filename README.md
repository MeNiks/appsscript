### Distance Calaulation

```
function CALCULATE_DRIVING_DISTANCE(origin, destination) {
    // origin= \"Pune\"
    // destination= \"Nanded\"
    var directions = Maps.newDirectionFinder()
        .setOrigin(origin)
        .setDestination(destination)
        .setMode(Maps.DirectionFinder.Mode.DRIVING)
        .getDirections();

    var distance = directions.routes[0].legs[0].distance.value;

    distance /= 1000; // Convert meters to kilometers
    return Number(distance.toFixed(2));
}

function CALCULATE_DRIVING_DURATION(origin, destination) {
    // origin= \"Pune\"
    // destination= \"Nanded\"
    var directions = Maps.newDirectionFinder()
        .setOrigin(origin)
        .setDestination(destination)
        .setMode(Maps.DirectionFinder.Mode.DRIVING)
        .getDirections();
    return directions.routes[0].legs[0].duration.text
}

```
