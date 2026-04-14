# AKS GPU Autoscaling Pattern

## Problem
- GPU workloads need efficient scaling
- CPU-based scaling is insufficient
- multiple scaling approaches exist

## Options
- HPA (CPU/memory)
- KEDA
- Prometheus + GPU metrics

## Decision
- Prometheus + GPU metrics

## Why
- reflects actual GPU utilization
- integrates with Kubernetes scaling

## Scope
- not production system
- prove GPU-based scaling works

## Experiments
- expose GPU metrics (DCGM)
- validate in Prometheus
- connect Prometheus Adapter
- trigger HPA

## Result
- GPU metrics available
- scaling triggered correctly

## Pattern
Autoscale GPU workloads using:
Prometheus + DCGM + Adapter + HPA
