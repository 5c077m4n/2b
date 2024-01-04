- `[someId]`: when this is a dir/file name then then in the component's props I can use it as:

```tsx
type AppProps = {
	params: { someId: string };
};
export default function App({ params: { someId } }: AppProps): JSX.Element {
	return null;
}
```

- `[...slug]`: this is a catch all for a route - `/whatever/[...slug]` will catch anything after the first `/whatever/` part of the URL
- `[[...slug]]`: optional slug - the same as before but this time it's optional (in the prev bullet the route `/whatever/` alone is invalid)
- `(some-group)`: is a dir that all it does is group routes together for better folder hierarchy (and does not change the URLs used at all)
