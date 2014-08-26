Modular Scale for Less
======================

Modular Scale for Less. Ported from [Bourbon Sass](https://github.com/thoughtbot/bourbon "Bourbon Sass").

Usage
-----

```less
@import "modular-scale";

// Defaults values
@modular-scale-sizes : 14, 44;
@modular-scale-ratio : @golden;
@modular-scale-unit  : px;

p {
	.modular-scale(1);
	font-size: @modular-scale-return;
}

// Outputs
p {
	font-size: 16.8072106px;
}
```

Parameters? Of course!

```less
p {
  .modular-scale(@pos: 5; @sizes: 16; @ratio: @minor-third; @unit: em);
  font-size: @modular-scale-return;
}

// Outputs
p {
  font-size: 39.81312em;
}
```

Negative positions, yay!

```less
small {
  .modular-scale(-2);
  font-size: @modular-scale-return;
  & {
    .modular-scale(-3);
    margin-bottom: @modular-scale-return;
  }
}

// Outputs
small {
  font-size: 8.6526576px;
  margin-bottom: 6.42005291px;
}
```
