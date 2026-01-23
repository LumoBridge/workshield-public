<div align="center" style="
  background:#020617;
  border:1px solid #1e293b;
  border-radius:16px;
  padding:24px 20px;
  margin-bottom:28px;
">

  <img
    src="https://raw.githubusercontent.com/Vey-Digital/workshield-public/main/workShield_ExSum-3.png"
    alt="WorkShield Executive Summary"
    width="90%"
    style="max-width:1200px; display:block; margin:0 auto;"
  />

</div>
export default function PlatformComparisonTable() {
  return (
    <section className="mt-12 overflow-hidden rounded-2xl border border-slate-800 bg-slate-950/60 backdrop-blur">
      <div className="overflow-x-auto">
        <table className="w-full border-collapse text-sm">
          <thead>
            <tr className="border-b border-slate-800 bg-slate-900/60">
              <th className="px-4 py-3 text-left font-semibold text-slate-300">
                Capability
              </th>
              <th className="px-4 py-3 text-left font-semibold text-slate-100">
                Managed application data platform (WorkShield)
              </th>
              <th className="px-4 py-3 text-left font-semibold text-slate-300">
                AWS
              </th>
              <th className="px-4 py-3 text-left font-semibold text-slate-300">
                Azure
              </th>
            </tr>
          </thead>
          <tbody className="divide-y divide-slate-800">
            {[
              [
                "PostgreSQL database",
                "Managed PostgreSQL service",
                "RDS / Aurora",
                "Azure Database for PostgreSQL",
              ],
              [
                "Authentication",
                "Integrated authentication service",
                "Cognito",
                "Entra ID / B2C",
              ],
              [
                "File storage",
                "Integrated object storage",
                "S3",
                "Blob Storage",
              ],
              [
                "Row-level security",
                "Native database-level policies",
                "Custom implementation",
                "Custom implementation",
              ],
              [
                "Realtime",
                "Integrated realtime subscriptions",
                "AppSync / custom",
                "SignalR",
              ],
              [
                "Edge / serverless functions",
                "Integrated function runtime",
                "Lambda",
                "Azure Functions",
              ],
              [
                "Backups",
                "Managed automated backups",
                "Separate configuration",
                "Separate configuration",
              ],
              [
                "IAM / access control",
                "Platform-level access controls",
                "IAM service configuration",
                "IAM service configuration",
              ],
              [
                "Setup time",
                "Application-oriented provisioning",
                "Infrastructure provisioning",
                "Infrastructure provisioning",
              ],
            ].map(([capability, workshield, aws, azure]) => (
              <tr key={capability} className="hover:bg-slate-900/40 transition-colors">
                <td className="px-4 py-3 font-medium text-slate-300">
                  {capability}
                </td>
                <td className="px-4 py-3 text-slate-100">
                  {workshield}
                </td>
                <td className="px-4 py-3 text-slate-300">
                  {aws}
                </td>
                <td className="px-4 py-3 text-slate-300">
                  {azure}
                </td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>

      <div className="border-t border-slate-800 bg-slate-900/40 px-4 py-3 text-xs text-slate-400">
        WorkShield is delivered as a managed application data platform integrating secure data storage,
        access controls, and documentation workflows. It does not replace enterprise infrastructure providers.
      </div>
    </section>
  );
}
