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

## Second-order effects
- Prometheus becomes a required dependency in the cluster
- DCGM Exporter must run as DaemonSet — affects node resource budget
- HPA lag under burst load may cause under-provisioning windows

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

## Prototype
- deploy single GPU pod with DCGM Exporter sidecar
- install Prometheus (kube-prometheus-stack)
- install Prometheus Adapter with GPU metric config
- apply HPA targeting `nvidia_gpu_duty_cycle`

## Pattern
Autoscale GPU workloads using:
Prometheus + DCGM + Adapter + HPA
