---
title: "3 - HitByBulletEvent"
tags:
  - robocode
  - tutorial
  - hands-on
  - cs
  - intermediate
---

## 4 – Dodge When Hit (Super Simple)

When a bullet hits your robot, the `onHitByBullet` method runs.

### What happens?

- Robocode tells your bot, “You were hit!”
- We’ll just turn and drive away — no tricky math.

### Code

```java
@Override
public void onHitByBullet(HitByBulletEvent e) {
    // 1. Turn 90° from our current direction
    turnRight(90);

    // 2. Drive forward to a new spot
    forward(120);
}
```

That’s it! Your robot takes a quick sidestep and keeps rolling.

### Why it works

- Turning 90° gets you off the line the bullet was travelling.
- Driving forward puts distance between you and the danger.

### Next idea

If you want to get fancy later, you can check where you are on the field with:

```java
double x = getX();
double y = getY();
```

…and use `getDirection()` to decide which way is safest.

But for now, this two‑line dodge keeps things simple and fun.

[Minigame](/robocode/Day-4/04_minigame)

## Navigation

⬅️ [Back: ScannedRobotEvent](/robocode/Day-4/01_scanned_robot_event)
➡️ [Next: Day 5](/robocode/Day-5/index)
