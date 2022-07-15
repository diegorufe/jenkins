MAX_BUILDS = 5
MAX_MASTER_BUILDS = 20

//Delete all builds from master branch jobs(except last 20)
for (job in Jenkins.instance.items) {
  if (job instanceof jenkins.branch.MultiBranchProject) {
    job = job.getJob("master")
    if (job != null) {
      def recent = job.builds.limit(MAX_MASTER_BUILDS)
      for (build in job.builds) {
        if (!recent.contains(build)) {
          build.delete()
          println "Deleted to delete: " + build
        }
      }
    }
  }
}

//Delete all builds from development branch jobs(except last 5)
for (job in Jenkins.instance.items) {
  if (job instanceof jenkins.branch.MultiBranchProject) {
    job = job.getJob("development")
    if (job != null) {
      def recent = job.builds.limit(MAX_BUILDS)
      for (build in job.builds) {
        if (!recent.contains(build)) {
          build.delete()
          println "Deleted to delete: " + build
        }
      }
    }
  }
}

//Delete all builds from test branch jobs(except last 5)
for (job in Jenkins.instance.items) {
  if (job instanceof jenkins.branch.MultiBranchProject) {
    job = job.getJob("test")
    if (job != null) {
      def recent = job.builds.limit(MAX_BUILDS)
      for (build in job.builds) {
        if (!recent.contains(build)) {
          build.delete()
          println "Deleted to delete: " + build
        }
      }
    }
  }
}

//Delete all builds from qc branch jobs(except last 5)
for (job in Jenkins.instance.items) {
  if (job instanceof jenkins.branch.MultiBranchProject) {
    job = job.getJob("qc")
    if (job != null) {
      def recent = job.builds.limit(MAX_BUILDS)
      for (build in job.builds) {
        if (!recent.contains(build)) {
          build.delete()
          println "Deleted to delete: " + build
        }
      }
    }
  }
}
