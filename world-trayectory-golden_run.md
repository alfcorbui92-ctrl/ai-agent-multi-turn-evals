# Golden Run (Final run)

## TURN 1 | ACT → YIELD
Request missing full itinerary details, passenger info, and constraints.

## TURN 2 | ACT
Retrieve all available flights for each segment of the itinerary.

## TURN 3 | ACT
Filter results to flights departing before 11AM.

## TURN 4 | ACT → YIELD
Re-evaluate itinerary due to updated Paris date constraint.

## TURN 5 | ACT
Execute booking for all confirmed flights using provided payment method.

## TURN 6 | ACT
Switch context to email system and respond to all incoming invitations with updated arrival dates.

# Hints Used (Final run only)

## Turn 1
[USER HINT] Confirm full itinerary before performing any booking actions.

## Turn 4
[USER HINT] The Paris leg date has changed and invalidates previous assumptions.

## Turn 6
[USER HINT] Use finalized itinerary to extract arrival dates before responding to emails.
