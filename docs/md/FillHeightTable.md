### Fill height

<!--start-code-->

```js
const App = () => {
  const [height, setHeight] = React.useState(30);
  const [fillHeight, setFillHeight] = React.useState(false);

  const data = fakeData.filter((item, index) => index < 50);
  return (
    <div>
      <Stack spacing={10} divider={<Divider vertical />}>
        <span>
          <Checkbox
            checked={fillHeight}
            onChange={(_v, checked) => {
              setFillHeight(checked);
            }}
          >
            fillHeight
          </Checkbox>
        </span>

        <span>
          Container height:{' '}
          <Input
            type="text"
            style={{ width: 100, display: 'inline-block' }}
            onChange={setHeight}
            value={height}
          />{' '}
          rem
        </span>
      </Stack>
      <hr />
      <div style={{ border: '1px solid red', height: `${height}rem` }}>
        <Table
          height={400}
          fillHeight={fillHeight}
          data={data}
          onRowClick={data => {
            console.log(data);
          }}
        >
          <Column width={70} align="center">
            <HeaderCell>Id</HeaderCell>
            <Cell dataKey="id" />
          </Column>

          <Column width={130}>
            <HeaderCell>First Name</HeaderCell>
            <Cell dataKey="firstName" />
          </Column>

          <Column width={130}>
            <HeaderCell>Last Name</HeaderCell>
            <Cell dataKey="lastName" />
          </Column>

          <Column width={200}>
            <HeaderCell>City</HeaderCell>
            <Cell dataKey="city" />
          </Column>

          <Column width={200}>
            <HeaderCell>Street</HeaderCell>
            <Cell dataKey="street" />
          </Column>

          <Column width={200}>
            <HeaderCell>Company Name</HeaderCell>
            <Cell dataKey="companyName" />
          </Column>

          <Column width={200}>
            <HeaderCell>Email</HeaderCell>
            <Cell dataKey="email" />
          </Column>

          <Column width={200}>
            <HeaderCell>Email</HeaderCell>
            <Cell dataKey="email" />
          </Column>

          <Column width={200}>
            <HeaderCell>Email</HeaderCell>
            <Cell dataKey="email" />
          </Column>

          <Column width={200}>
            <HeaderCell>Email</HeaderCell>
            <Cell dataKey="email" />
          </Column>
        </Table>
      </div>
    </div>
  );
};
ReactDOM.render(<App />);
```

<!--end-code-->
