# Powerlevel CC

?> CommandClass ID: `0x73`

## Powerlevel CC methods

### `setNormalPowerlevel`

```ts
async setNormalPowerlevel(): Promise<SupervisionResult | undefined>;
```

### `setCustomPowerlevel`

```ts
async setCustomPowerlevel(
	powerlevel: Powerlevel,
	timeout: number,
): Promise<SupervisionResult | undefined>;
```

### `getPowerlevel`

```ts
async getPowerlevel(): Promise<
	MaybeNotKnown<Pick<PowerlevelCCReport, "powerlevel" | "timeout">>
>;
```

### `reportPowerlevel`

```ts
async reportPowerlevel(
	options: PowerlevelCCReportOptions,
): Promise<void>;
```

### `startNodeTest`

```ts
async startNodeTest(
	testNodeId: number,
	powerlevel: Powerlevel,
	testFrameCount: number,
): Promise<SupervisionResult | undefined>;
```

### `getNodeTestStatus`

```ts
async getNodeTestStatus(): Promise<
	MaybeNotKnown<
		Pick<
			PowerlevelCCTestNodeReport,
			"testNodeId" | "status" | "acknowledgedFrames"
		>
	>
>;
```

### `sendNodeTestReport`

```ts
async sendNodeTestReport(
	options: PowerlevelCCTestNodeReportOptions,
): Promise<void>;
```
