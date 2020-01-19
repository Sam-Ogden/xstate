# xstate

## 4.7.7

### Patch Changes

- c8db035: The `escalate()` action can now take in an expression, which will be evaluated against the `context`, `event`, and `meta` to return the error data.
- 2a3fea1: The typings for the raise() action have been fixed to allow any event to be raised. This typed behavior will be refined in version 5, to limit raised events to those that the machine accepts.

## 4.7.6

### Patch Changes

- dae8818: Typestates are now propagated to interpreted services.

## 4.7.5

### Patch Changes

- 6b3d767: Fixed issue with delayed transitions scheduling a delayed event for each transition defined for a single delay.

## 4.7.4

### Patch Changes

- 9b043cd: The initial state is now cached inside of the service instance instead of the machine, which was the previous (faulty) strategy. This will prevent entry actions on initial states from being called more than once, which is important for ensuring that actors are not spawned more than once.

## 4.7.3

### Patch Changes

- 2b134eee: Fixed issue with events being forwarded to children after being processed by the current machine. Events are now always forwarded first.
- 2b134eee: Fixed issue with not being able to spawn an actor when processing an event batch.
