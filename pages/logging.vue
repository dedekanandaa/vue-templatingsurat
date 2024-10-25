<template>
    <div class="p-4 bg-gray-100 min-h-screen">
        <div class="max-w-5xl mx-auto bg-white rounded-lg shadow-md p-6">
            <h2 class="text-2xl font-semibold text-gray-800 mb-4">Logging Table</h2>
            
            <!-- Tabel Log -->
            <div class="overflow-x-auto">
                <table class="w-full text-sm text-left text-gray-500">
                    <thead class="text-xs uppercase bg-gray-200 text-gray-700">
                        <tr>
                            <th scope="col" class="px-4 py-2">ID Log</th>
                            <th scope="col" class="px-4 py-2">Tanggal/Waktu</th>
                            <th scope="col" class="px-4 py-2">Jenis Log</th>
                            <th scope="col" class="px-4 py-2">Deskripsi</th>
                            <th scope="col" class="px-4 py-2">User</th>
                            <th scope="col" class="px-4 py-2">Lokasi</th>
                        </tr>
                    </thead>
                    <tbody>
                        <!-- Contoh data log -->
                        <tr class="bg-white border-b">
                            <td class="px-4 py-2 font-medium text-gray-900">1</td>
                            <td class="px-4 py-2">2024-10-25 10:30:45</td>
                            <td class="px-4 py-2">Template Surat</td>
                            <td class="px-4 py-2">Hapus Template.</td>
                            <td class="px-4 py-2">Admin</td>
                            <td class="px-4 py-2">Kantor Pusat</td>
                        </tr>
                        <tr class="bg-gray-50 border-b">
                            <td class="px-4 py-2 font-medium text-gray-900">2</td>
                            <td class="px-4 py-2">2024-10-25 11:15:20</td>
                            <td class="px-4 py-2">Surat Peminjaman</td>
                            <td class="px-4 py-2">Surat Di-Approve.</td>
                            <td class="px-4 py-2">Manajer</td>
                            <td class="px-4 py-2">Cabang Jakarta</td>
                        </tr>
                        <tr class="bg-white border-b">
                            <td class="px-4 py-2 font-medium text-gray-900">3</td>
                            <td class="px-4 py-2">2024-10-25 12:45:10</td>
                            <td class="px-4 py-2">Surat Ijin</td>
                            <td class="px-4 py-2">Surat Ditolak.</td>
                            <td class="px-4 py-2">Supervisor</td>
                            <td class="px-4 py-2">Cabang Bandung</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>
