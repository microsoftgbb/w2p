# Whiteboard to Rapid Prototype (W2P)

Validate architecture decisions quickly by building minimal working prototypes.

Reduce uncertainty. Unblock customers. Generate reusable patterns.

## Usage

Fill out `brief.md` after a whiteboard session:

```
# Project Goal, Current State, Requirements, Future Vision, Constraints, Parking Lot
```

Then run inside VS Code:

```
/idea #file:brief.md
```

Or skip the brief for a quick idea:

```
/idea Autoscale GPU workloads in AKS based on real GPU utilization
```

## What it does

- frames architecture options
- surfaces second-order effects
- identifies risks and constraints
- defines a minimal validation path

## Flow

Whiteboard → W2P → Pattern → Accelerator → Full Solution

## Notes

- not a replacement for ADS
- not production engineering
- designed to reduce decision time
- feeds Pattern repos and solution accelerators such as Project Stormbreaker

## Example

See `/examples/aks-gpu-autoscale/` for a real W2P validating AKS GPU autoscaling architecture.
