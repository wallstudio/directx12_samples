# directx12_samples
DirectX12本に添付するサンプルプログラム
+ なお、逐次VS2019用に移行するため以前のVS2017用のプログラムはBackupForVS2017フォルダに移動しています

# GPU Based Validationエラー誘発版

マテリアルDescriptorHeapのCBVを取り除きSRVだけにしたことにより、以下のエラーが発生する。

> D3D12 ERROR: GPU-BASED VALIDATION: Draw,
>	Descriptor type doesn't match shader register type: Descriptor Heap Index To DescriptorTableStart: [0],
>	Descriptor Heap Index FromTableStart: [0],
>	Descriptor Type in Heap: D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
>	Register Type: D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
>	Index of Descriptor Range: 0,
>	Shader Stage: VERTEX,
>	Root Parameter Index: [0],
>	Draw Index: [0],
>	Shader Code: C:\Users\huser\Desktop\directx12_samples\Chapter8\BasicVertexShader.hlsl(24,2-23),
>	Asm Instruction Range: [0x94-0xb3],
>	Asm Operand Index: [2],
>	Command List: 0x000002B30DFAE2B0:'Unnamed ID3D12GraphicsCommandList Object',
>	SRV/UAV/CBV Descriptor Heap: 0x000002B30E265E60:'Unnamed ID3D12DescriptorHeap Object',
>	Sampler Descriptor Heap: <not set>,
>	Pipeline State: 0x000002B30E613E10:'Unnamed ID3D12PipelineState Object',
>	[ EXECUTION ERROR #939: GPU_BASED_VALIDATION_DESCRIPTOR_TYPE_MISMATCH]
