# Jest

## Basic test

```js
describe('makePoniesPink', () => {
  it('should make each pony pink', () => {
    const actual = fn(['Alice', 'Bob', 'Eve']);
    expect(actual).toEqual(['Pink Alice', 'Pink Bob', 'Pink Eve']);
  });
});
```

## Matchers

```js
expect.assertions(28)

expect(42).toBe(42)
expect(42).not.toBe(3)
expect([1, 2]).toEqual([1, 2])
expect('foo').toBeTruthy()
expect('').toBeFalsy()
expect(null).toBeNull()
expect(undefined).toBeUndefined()
expect(7).toBeDefined()

expect('long string').toMatch('str')
expect(result).toMatch(/regexp/)

expect({a: 1, b: 2}).toMatchObject({a: 1})

expect(2).toBeGreaterThan(1)
expect(1).toBeGreaterThanOrEqual(1)
expect(1).toBeLessThan(2)
expect(1).toBeLessThanOrEqual(1)
expect(0.2 + 0.1).toBeCloseTo(0.3, 5)

expect(['Alice', 'Bob', 'Eve']).toHaveLength(3)
expect(['Alice', 'Bob', 'Eve']).toContain('Alice')
expect([{a: 1}, {a: 2}]).toContainEqual({a: 1})
expect(['Alice', 'Bob', 'Eve']).toEqual(expect.arrayContaining(['Alice', 'Bob']))

expect(new A()).toBeInstanceOf(A)

expect(node).toMatchSnapshot()

expect(fn).toThrow()
expect(fn).toThrow('Out of cheese')
expect(fn).toThrowErrorMatchingSnapshot()

expect(fn).toBeCalled()
expect(fn).toHaveBeenCalledTimes(1)
expect(fn).toBeCalledWith(expect.stringContaining('foo'))
expect(fn).toBeCalledWith(expect.stringMatching(/^[A-Z]\d+$/))
expect(fn).toBeCalledWith(expect.objectContaining({x: expect.any(Number), y: expect.any(Number)}))
expect(fn).toHaveBeenLastCalledWith(expect.anything())
```

[Matchers docs](https://facebook.github.io/jest/docs/expect.html)

## Mock functions

```js
it('should call the callback', () => {
  const callback = jest.fn();
  fn(callback);
  expect(callback).toBeCalled();
  expect(callback.mock.calls[0][1].baz).toBe('pizza'); // Second argument of the first call
});
```

[Mock functions docs](https://facebook.github.io/jest/docs/mock-function-api.html)

## Resources

* [Jest site](https://facebook.github.io/jest/)
* [Testing React components with Jest and Enzyme](http://blog.sapegin.me/all/react-jest) by Artem Sapegin
* [Testing React Applications](https://youtu.be/59Ndb3YkLKA) by Max Stoiber
* [Migrating to Jest](https://medium.com/@kentcdodds/migrating-to-jest-881f75366e7e#.pc4s5ut6z) by Kent C. Dodds
* [Migrating AVA to Jest](http://browniefed.com/blog/migrating-ava-to-jest/) by Jason Brown
- [Testing Javascript with Jest](https://egghead.io/playlists/testing-javascript-with-jest-a36c4074)
