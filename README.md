# Whiteboard to Rapid Prototype (W2P)

W2P is a lightweight approach to validate architecture decisions quickly by building minimal working prototypes.

It is used to reduce uncertainty, unblock customers, and generate reusable patterns.

## Usage

Run inside VS Code:

```
/idea <your idea>
```

Example:

```
/idea Autoscale GPU workloads in AKS based on real GPU utilization
```

---

## What it does

- frames architecture options
- surfaces second-order effects
- identifies risks and constraints
- defines a minimal validation path

---

## Flow

Whiteboard → W2P → Pattern → Accelerator → Full Solution

## Output

- working prototype
- validated decision
- candidate pattern

## Context

This approach is used to produce Pattern repositories and inform larger solution accelerators such as Project Stormbreaker.

## Notes

- not a replacement for ADS
- not a replacement for full architecture design
- not production engineering
- designed to reduce decision time

## Example

See `/examples/aks-gpu-autoscale/` for a real W2P application validating AKS autoscaling architecture.
