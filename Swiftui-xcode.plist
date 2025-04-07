import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack {
            Color.black.ignoresSafeArea()

            VStack(spacing: 30) {
                Text("GargetSign")
                    .font(.largeTitle)
                    .fontWeight(.bold)
                    .foregroundColor(.white)

                Text("Sign and Install IPA files easily.")
                    .foregroundColor(.gray)
                    .multilineTextAlignment(.center)

                Button(action: {
                    installIPA()
                }) {
                    Text("Install IPA")
                        .font(.title2)
                        .fontWeight(.semibold)
                        .padding()
                        .frame(maxWidth: .infinity)
                        .background(LinearGradient(gradient: Gradient(colors: [Color.red, Color.pink]), startPoint: .leading, endPoint: .trailing))
                        .cornerRadius(20)
                        .shadow(color: .red.opacity(0.5), radius: 10, x: 0, y: 5)
                        .foregroundColor(.white)
                        .padding(.horizontal)
                }
            }
            .padding()
        }
    }

    func installIPA() {
        let manifestURL = "https://yourdomain.com/manifest.plist" // <- change this
        if let url = URL(string: "itms-services://?action=download-manifest&url=\(manifestURL)") {
            UIApplication.shared.open(url)
        }
    }
}

#Preview {
    ContentView()
}
