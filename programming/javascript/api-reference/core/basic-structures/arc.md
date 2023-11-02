---
layout: default-layout
title: interface Arc - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Arc in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Arc

The `Arc` interface defines the structure of a "arc" shape in 2-dimensional space.

## Definition

```typescript
interface Arc {
    x: number;
    y: number;
    radius: number;
    startAngle: number;
    endAngle: number;
} 
```

| Properties                  | Type     |
| --------------------------- | -------- |
| [`x`](#x)                   | *number* |
| [`y`](#y)                   | *number* |
| [`radius`](#radius)         | *number* |
| [`startAngle`](#startangle) | *number* |
| [`endAngle`](#endangle)     | *number* |

### x

The x-coordinate of the center point of the arc.

```typescript
x: number;
```

### y

The y-coordinate of the center point of the arc.

```typescript
y: number;
```

### radius

The radius of the arc.

```typescript
radius: number;
```

### startAngle

The starting angle of the arc in radians.

```typescript
startAngle: number;
```

### endAngle

The ending angle of the arc in radians.

```typescript
endAngle: number;
```
