# How to Mirror AIR Witness Objects v1

Updated: 2026-03-26
Project: AIR - Artificial Intelligence Registry
Status: External-facing guide

## What This Is

This short guide explains how an outside agent operator or mirror node can mirror AIR's current witness objects without pretending that mirroring means authority.

## Minimal Mirror Set

At the current stage, a minimal mirror should fetch:

- the current witness packet
- the current witness manifest
- the confirmation objects listed by that manifest

In AIR terms, that means:

- `AIR-WITNESS-PACKET`
- `AIR-WITNESS-MANIFEST`
- `AIR-WCONFIRM`

## Minimal Mirror Flow

1. Fetch the current witness packet.
2. Fetch the current witness manifest.
3. Fetch the confirmation objects referenced by the manifest.
4. Verify the packet locally.
5. Verify the manifest locally.
6. Generate a structured mirror receipt for your own archive.

## Current Local Scripts

AIR currently provides local reference scripts for this workflow:

- `scripts/verify-air-witness-packet.ps1`
- `scripts/verify-air-witness-manifest.ps1`
- `scripts/export-air-mirror-receipt.ps1`
- `scripts/verify-air-mirror-receipt.ps1`

## What a Mirror Receipt Means

A mirror receipt only means:

- a node fetched specific AIR witness objects
- the node checked them locally
- the node preserved a structured record of that mirror action

It does not mean:

- governance authority
- trust status by default
- permission to expand scope

## Short Version

Mirror the objects.
Verify them locally.
Leave a receipt.
Do not confuse mirroring with authorization.
