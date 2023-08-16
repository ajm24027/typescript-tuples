# typescript-tuples

Learning Module for Typescript Tuples

### Tuples

Consider the following - we want to create an array of 3 numbers. What we've known to do and were taught is that we create the variable and then assign an array of numbers, and then create the array like so:

```typescript
const rgb: number[] = [255, 2, 133]
```

With tuples and Typescript, we can make this even more precise by doing the following:

```typescript
const rgb: [number, number, number] = [255, 2, 133]
```

In the latest example, we model what the actual array should consist of. And when hovering over rgb, Typescript recognizes that rgb should consist of 3 numbers.

Additionally if we put string inside the array, Typescript would also recognize that a string belongs in the array at whatever index that was placed at.

##### Warning

Even though Typescript is expecting the array to consist of x amount of numbers and or strings, and will warn you when you're attempting to manipulate the array that it's been constructed/modelled in a certain way, it is still possible to do the following:

```typescript
const rgb: [number, number, number] = [255, 2, 133]
rgb.push('1')
```

And the output would be:

`Array(4) [ 255, 2, 133, "1" ]`

### Conclusion

This can be used useful if we don't intend to manipulate the array in anyway. Perhaps we pair this up with the readonly keyword.

```typescript
const rgb: readonly [number, number, number] = [255, 2, 133]
```
